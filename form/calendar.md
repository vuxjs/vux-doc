# Calendar 日历

> `Calendar`组件直接依赖于`InlineCalendar`+`Popup` 

## 与Datetime的使用场景差别

+ `calendar` 不支持具体钟点选择，因此需要选择具体时间时需要使用 `datetime`
+ `calendar` 支持范围选择，如果使用`datetime`需要使用两次来分别选择开始时间和结束时间
+ `calendar` 更适合于需要更好展现整个月信息及星期信息的情况，如跨月的日程安排， `datetime`更适合于选择距离今天不远的日期场景，如近期任务安排


## Props

日历相关属性同 [`inline-calendar`](inline-calendar.md)

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| title | String | 无 | cell标题 |

## Demo

``` html
<group>
  <calendar :value.sync="value" title="Date Picker"></calendar>
</group>
```
