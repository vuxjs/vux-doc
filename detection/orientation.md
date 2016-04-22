# 横竖屏切换提示

此组件以指令的形式控制DOM在横竖屏下的显示，支持的选项有

* landscape - 当横屏时显示
* portrait - 当竖屏时显示

[查看在线DEMO](https://vux.li/#!/component/orientation)

```
<template>
  <div>
    <div v-orientation="landscape" class="landscape"><div>竖屏观看更合适哦</div></div>
    <div v-orientation="portrait" class="portrait"><div>翻转手机看效果</div></div>
  </div>
</template>
<script>
export default {
  directives: {
    Orientation
  }
}
</script>
```
