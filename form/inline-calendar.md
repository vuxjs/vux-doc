# Inline Calendar

## Props

| 参数         |      类型       |     默认值     |    说明    |
| ----------- | -------------- | ---------- | ------- |
| value | String | 无 | 当前选中日期，双向绑定，默认为空，即选中当天日期 |
| start-date | String | 无 | 可选起始日期，格式为'YYYY-MM-dd' |
| end-date | String | 无 | 可选结束日期，格式为'YYYY-MM-dd' |
| render-month | Array | 无 | 可选，指定渲染日期，如 [2018, 8] |
| show-last-month | Boolean | true | 是否显示上个月的日期 |
| show-next-month | Boolean | true | 是否显示下个月的日期 |
| highlight-weekend | Boolean | false | 是否高亮周末 |
| return-six-rows | Boolean | true | 是否总是渲染6行日期 |
| hideHeader | Boolean | false | 是否隐藏日历头部 |
| hiddeWeekList | Boolean | false | 是否隐藏星期列表 |
| replace-text-list | Object | {} | 替换列表，可以将默认的日期换成文字，比如今天的日期替换成`今`，{'TODAY':'今'} |
| weeks-list | Array | ['Su', 'Mo', 'Tu', 'We', 'Th', 'Fr', 'Sa'] | 导航星期列表，从周日开始 |
| custom-slot-fn | Function | 无 | 用于为特定日期添加额外的html内容，参数为(行index,列index,日期详细属性) |
| render-on-value-chhange | Boolean | true | 当日期变化时是否重新渲染日历，如果是渲染了多个日历的话需要设为false |
| disable-past | Boolean | false | 禁止选择过去的日期，该选项可以与start-date同时使用 |

## demos

> PC文档样式会有偏差，后面修复。

### 设置开始和结束时间

``` vux height=300 components=InlineCalendar
<template>
<inline-calendar start-date="2016-06-04" end-date="2017-06-18"></inline-calendar>
</template>
```

### 不显示上个月和下个月的日期
``` vux height=300 components=InlineCalendar
<template>
<inline-calendar :show-next-month="false" :show-last-month="false"></inline-calendar>
</template>
```

### 取值
``` vux height=400 components=InlineCalendar,Group,Cell
<template>
<inline-calendar :value.sync="value"></inline-calendar>
<group>
  <cell title="current value" :value="value"></cell>
</group>
</template>

<script>
export default {
  data () {
    return {
      value: 'TODAY'
    }
  }
}
</script>
```