# datetime 时间

## 属性

+ format 显示格式，默认是'YYYY-MM-DD'
+ title 显示标题，非空
+ value 日期值
+ inline-desc 副标题
+ placeholder 提示文字
+ min-year 最小可选年
+ max-year 最大可选年
+ confirm-text 确认按钮文字，默认为'ok'
+ cancel-text 取消按钮文字，默认为'cancel'
+ year-row 年份显示格式
+ month-row 月份显示格式
+ day-row 日期显示格式
+ hour-row 小时显示格式
+ minute-row 分钟显示格式

## demos

``` html
<datetime title="select a date"></datetime>
<!-- 可选分钟 -->
<datetime title="select minutes" format="YYYY-MM-DD HH:mm"></datetime>
<!-- 设置最小和最大可选年 -->
<datetime 
    title="specify min-year and max-year"
    :min-year=2000 
    :max-year=2016
    value="please select"></datetime>
<!-- 自定义确认按钮和取消按钮文字 -->
<datetime
    title="自定义按钮文字"
    confirm-text="确认"
    cancel-text="取消"></datetime>
<!-- 自定义时间显示文字 -->
<datetime
    title="xx年xx月xx日xx点xx分"
    year-row="{value}年"
    month-row="{value}月"
    day-row="{value}日"
    hour-row="{value}点"
    minute-row="{value}分"></datetime>
<!-- change事件 -->
<datetime
    title="change事件"
    @change="change"></datetime>

<script>
export default {
    methods:{
        change (val) {
            console.log('change',val)
        }
    }
}
</script>
```
