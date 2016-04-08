# Tab 选项卡

### 基本粟子

{% vux height=50,components="Tab,TabItem" %}
<template>
<tab>
  <tab-item :selected="demo1 === '已发货'" @click="demo1 = '已发货'">已发货</tab-item>
  <tab-item :selected="demo1 === '未发货'" @click="demo1 = '未发货'">未发货</tab-item>
  <tab-item :selected="demo1 === '全部订单'" @click="demo1 = '全部订单'">全部订单</tab-item>
</tab>
</template>

<script>
export default {
  data: {
    demo1: '未发货'
  }
}
</script>
{% endvux %}

### 更简洁的粟子

{% vux height=50,components="Tab,TabItem" %}
<template>
<tab :line-width=2 active-color='#fc378c'>
  <tab-item :selected="demo2 === item" v-for="item in list2" @click="demo2 = item"><<item>></tab-item>
</tab>
</template>

<script>
export default {
  data: {
    demo2: '美食',
    list2: ['精选', '美食', '电影', '酒店', '外卖']
  }
}
</script>
{% endvux %}


### 禁用滑动动画

{% vux height=50,components="Tab,TabItem" %}
<template>
<tab :line-width=1 :animate=false>
  <tab-item :selected="demo2 === item" v-for="item in list2" @click="demo2 = item"><<item>></tab-item>
</tab>
</template>

<script>
export default {
  data: {
    demo2: '美食',
    list2: ['精选', '美食', '电影', '酒店', '外卖']
  }
}
</script>
{% endvux %}
