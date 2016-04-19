# 行内日历

## 相比calendar的改进

+ 可独立显示，不需要放在父元素点击触发

## 属性

+ value 当前选中日期，双向绑定，默认为空，即选中当天日期
+ startDate 可选起始日期，格式为'yyyy-mm-dd'
+ endDate 可选结束日期，格式为'yyyy-mm-dd'
+ showLastMonth 是否显示上个月的日期，默认为true
+ showNextMonth 是否显示下个月的日期，默认为true
+ highlightWeekend 是否高亮周末，默认为false

## demos

``` html
<!-- 设置可选起始日期和可选结束日期 -->
<inline-calendar start-date="2016-06-04" end-date="2017-06-18"></inline-calendar>
<!-- 不显示上个月和下个月的日期 -->
<inline-calendar :show-next-month=false :show-last-month=false></inline-calendar>
<!-- 高光周末 -->
<inline-calendar :highlight-weekend=true></inline-calendar>
<!-- 双向绑定日期值 -->
<inline-calendar :value.sync="value"></inline-calendar>
<cell title="current value" :value="value"></cell>
```