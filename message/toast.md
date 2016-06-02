# Toast

## Props

| 参数         | 类型                 | 默认       | 说明 |
| ----------- | ---------------------- | ---------- | ------- |
| show  | Boolean | false | 是否显示，`双向绑定` |
| time  | Nummber  | 2000 | 显示时间 |
| type  | String   | success | 图标类型，可选为`success`,`text`,`cancel`,`warn` |
| transition | String | vux-fade | 动画 |
| width | String | `7.6em` | Toast宽度 |

> 尽管Toast组件提供了`cancel`和`warn`类型，但不推荐使用，需要用户关注的通知推荐使用`Alert`或者`Confirm`

## Slot

| 名字         | 说明            | 
| ----------- | --------------- | 
| 默认slot | 提示文字 |



## Demo

### 默认按钮文字

``` vux height=450 components=Toast,Group,Switch
<template>
<div>
  <group>
    <switch title="默认提示" :value.sync="show1"></switch>
    <switch title="文字提示" :value.sync="show2"></switch>
    <switch title="提示取消" :value.sync="show3"></switch>
    <switch title="提示禁止" :value.sync="show4"></switch>
    <switch title="设置出现时间1s" :value.sync="show5"></switch>
    <switch title="long text" :value.sync="show6"></switch>
  </group>
  <toast :show.sync="show1" >默认提示</toast>
  <toast :show.sync="show2" type="text">处理成功</toast>
  <toast :show.sync="show3" type="cancel">取消操作</toast>
  <toast :show.sync="show4" type="warn">禁止操作</toast>
  <toast :show.sync="show5" :time="1000">1s关闭</toast>
  <toast :show.sync="show6" type="text" width="20em">Talk is cheap, show me the code.</toast>
</div>
</template>

<script>
export default {
  data () {
    return {
      show1: false,
      show2: false,
      show3: false,
      show4: false,
      show5: false,
      show6: false
    }
  }
}
</script>
```