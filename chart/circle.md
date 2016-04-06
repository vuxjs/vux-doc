# 圆圈

## 应用场景

圆圈组件一般用于显示进度，展示百分比数据。


## 示例

### 简单示例

{% vux components="Circle" %}

<template>
<div style='width:100px;height:100px;'>
  <circle :percent=30 :stroke-width=10 stroke-color=#04BE02>
    <span>{{percent1}}</span>
  </circle>
</div>
</template>

{% endvux %}

### 添加中间内容

> 通过默认slot支持

{% vux components="Circle" %}

<template>
<div style='width:100px;height:100px;'>
  <circle :percent='percent2' :stroke-width=6 :trail-width=6 :stroke-color='strokeColor2' trail-color="#ececec">
    <span :style="{color: strokeColor2}"><<percent2>>%</span>
  </circle>
</div>
</template>

<script>
export default {
  ready () {
    setInterval(this.update, 2000)
  },
  data () {
    return {
      percent2: 30,
      strokeColor2: '#3FC7FA'
    }
  },
  methods: {
    update: function () {
      const colorMap = ['#3FC7FA', '#85D262', '#FE8C6A']
      this.percent2 = parseInt(Math.random() * 100, 10)
      this.strokeColor2 = colorMap[parseInt(Math.random() * 3, 10)]
    }
  }
}
</script>
{% endvux %}


