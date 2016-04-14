# Calendar 日历

## 与Datetime的使用场景差别

+ `calendar` 不支持具体钟点选择，因此需要选择具体时间时需要使用 `datetime`
+ `calendar` 支持范围选择，如果使用`datetime`需要使用两次来分别选择开始时间和结束时间
+ `calendar` 更适合于需要更好展现整个月信息及星期信息的情况，如跨月的日程安排， `datetime`更适合于选择距离今天不远的日期场景，如近期任务安排

## 属性

+ value 默认显示的内容，非空，通常是提示信息
+ hours 是否选择小时，默认为否
+ disablePast 是否禁止选择之前的日期，默认为否
+ dateList 自定义星期文字，默认是英文

## 基本使用

``` html
<calendar value="select date"></calendar>
```

## 配合Cell效果更佳

``` html
<cell title="选择小时">
    <calendar slot="value" value="select hours" hours></calendar>
</cell>
<cell title="禁止选择之前的日期">
    <calendar slot="value" value="select date" disablePast></calendar>
</cell>
<cell title="自定义星期文字">
    <calendar slot="value" value="chinese weekday" :data-list="dataList"></calendar>
</cell>

<script>
export default {
    data () {
        return {
            dateList: ['日', '一', '二', '三', '四', '五', '六']
        }
    }
}
</script>
```
