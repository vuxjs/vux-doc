# 日期格式化

轻量简单的日期格式化工具函数，毕竟很多时候我们并不想引入`moment`这个大块头。

可以引入`DateFormatter`组件作为`filter`, 参数为日期格式和时间及字符串格式。

``` vux height=50 components=Group filters=DateFormatter
<template>
<div>
  <span v-text="time1 | date-formatter 'YYYY-MM-DD'"></span>
  <br/>
  <span v-text="time2 | date-formatter 'YYYY-MM-DD HH:mm:ss'"></span>
</div>
</template>

<script>
export default {
  data: {
    time1: new Date('2016/01/03 19:19:19'),
    time2: new Date('2016-01-03 09:09:09')
  }
}
</script>
```