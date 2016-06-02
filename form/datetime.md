# datetime 时间

> 需要与`group`一起使用。

## Props

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| format | String | 'YYYY-MM-DD' | 显示格式 |
| title | String | 无 | 显示标题 |
| value | String | 默认为当前日期 | 日期值 |
| inline-desc | String | 无 | 副标题 |
| placeholder | String | 无 | 提示文字 |
| min-year | Number | 无 | 最小可选年 |
| max-year | Number | 无 | 最大可选年 |
| confirm-text | String | ok | 确认按钮文字 |
| cancel-text | String | cancel | 取消按钮文字 |
| year-row | String | {value} |年份显示格式 |
| month-row | String | {value} | 月份显示格式 |
| day-row | String | {value} | 日期显示格式 |
| hour-row | String | {value} | 小时显示格式 |
| minute-row | String | {value} | 分钟显示格式 |

## demos

``` html
<group>
  <datetime title="select a date"></datetime>
</group>

<!-- 可选分钟 -->
<group>
  <datetime title="select minutes" format="YYYY-MM-DD HH:mm"></datetime>
</group>

<!-- 设置最小和最大可选年 -->
<group>
  <datetime 
    title="specify min-year and max-year"
    :min-year=2000 
    :max-year=2016
    value="please select"></datetime>
</group>

<!-- 自定义确认按钮和取消按钮文字 -->
<gropu>
  <datetime
    title="自定义按钮文字"
    confirm-text="确认"
    cancel-text="取消"></datetime>
</gropu>

<!-- 自定义时间显示文字 -->
<group>
  <datetime
    title="xx年xx月xx日xx点xx分"
    year-row="{value}年"
    month-row="{value}月"
    day-row="{value}日"
    hour-row="{value}点"
    minute-row="{value}分"></datetime>
</group>

<!-- change事件 -->
<group>
  <datetime
    title="change事件"
    @change="change"></datetime>
</group>

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
