# Dialog

`Alert`及`Confirm`依赖于`Dialog`。

## Props

| 参数        | 类型        | 默认值 | 说明 |
| ----------- | ---------------------- | ---------- | ------- |
| show | Boolean | false | 是否显示，`双向绑定` |
| mask-transition | String | vux-fade | 遮罩动画 |
| dialog-transition | String | vux-dialog | 窗口动画 |

## Events

| 事件名       | 参数       | 说明 |
| ----------- | ---------------------- | ---------- |
| on-show | 无 | 显示时触发 |
| on-hide | 无 | 关闭时触发 |

## Slots

| 名字       | 说明       | 
| ----------- | ---------------------- | 
| 默认slot | 弹窗主体内容 | 

## Demo

``` html
<template>
  <div>
    <dialog :show.sync="show" class="dialog-demo">
      <p class="dialog-title">I'm a Dialog.</p>
    </dialog>
  </div>
</template>

```