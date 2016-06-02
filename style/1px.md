# 1px边框解决方案

## 应用场景

1px边框问题来源于在Retina屏幕下边框宽度大于1像素，略丑，解决方案来源于`FronzenUI`

一般用于`九宫格`等布局，在vux中配合`Flexbox`使用，常见于电商首页，支付工具服务列表页

## 使用

``` html
<style lang="less">
@import '~vux/src/styles/1px.less';
</style>
```
根据位置可用类名为：
+ `vux-1px-t`
+ `vux-1px-b`
+ `vux-1px-tb`
+ `vux-1px-l`
+ `vux-1px-r`

## 示例

``` vux height=180 components=Flexbox,FlexboxItem
<template>
  <flexbox class="vux-1px-tb" :margin-left=0 style="height:50px;">
    <flexbox-item class="vux-1px-r test"><div>北京</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>上海</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>广州</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>深圳</div></flexbox-item>
    <flexbox-item class="test"><div>其他</div></flexbox-item>
  </flexbox>
  <flexbox class="vux-1px-b" :margin-left=0 style="height:50px;">
    <flexbox-item class="vux-1px-r test"><div>天津</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>西安</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>重庆</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>杭州</div></flexbox-item>
    <flexbox-item class="test"><div>其他</div></flexbox-item>
  </flexbox>
  <flexbox class="vux-1px-b" :margin-left=0 style="height:50px;">
    <flexbox-item class="vux-1px-r test"><div>南京</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>武汉</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div>成都</div></flexbox-item>
    <flexbox-item class="vux-1px-r test"><div></div></flexbox-item>
    <flexbox-item class="test"><div>其他</div></flexbox-item>
  </flexbox>
</template>

<style>
.test{
  height:50px;
  text-align:center;
  line-height: 50px;
}
</style>
```