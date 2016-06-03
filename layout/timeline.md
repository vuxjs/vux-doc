# Timeline 时间轴

## Props

### timeline

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| color | 可选，线条颜色 | String | #04BE02 |


### Demo

``` vux height=250 components=Timeline,TimelineItem
<template>
<div class="timeline-demo">
  <timeline :color="color">
    <timeline-item>
      <h4 class="recent">【广东】 广州市 已发出</h4>
      <p class="recent">2016-04-17 12:00:00</p>
    </timeline-item>
    <timeline-item>
      <h4> 申通快递员 广东广州 收件员 xxx 已揽件</h4>
      <p>2016-04-16 10:23:00</p>
    </timeline-item>
    <timeline-item>
      <h4> 商家正在通知快递公司揽件</h4>
      <p>2016-04-15 9:00:00</p>
    </timeline-item>
  </timeline>
</div>
</template>
```

### 动态改变条目数量

``` vux height=600 components=Timeline,TimelineItem,XButton

<template>
<div class="timeline-demo">
  <timeline>
    <timeline-item v-for="i in count">
      <h4 :class="[i === 0 ? 'recent' : '']">Timeline Node {{i + 1}}</h4>
      <p :class="[i === 0 ? 'recent' : '']">index {{i + 1}}</p>
    </timeline-item>
  </timeline>
  <x-button type="primary" @click="count = 6"> Set to 6 nodes</x-button>
  <x-button type="primary" @click="count = 3"> Set to 3 nodes</x-button>
</div>
</template>
<script>
export default {
  data () {
    return {
      count: 3
    }
  }
}
</script>
<style>
  .timeline-demo p {
    color: #888;
    font-size: 0.8rem;
  }

  .timeline-demo h4 {
    color: #666;
    font-weight: normal;
  }

  .timeline-demo .recent {
    color: rgb(4, 190, 2);
  }
</style>
```
