# Flexbox

> Flexbox功能由`Flexbox`及`FlexboxItem`子组件组成。

> 当前的flexbox仅实现了子元素水平和垂直平分。

### 简单平分
```
<template>
<divider>Horizontal</divider>
<flexbox style="height:40px;">
  <flexbox-item><div class="flex-demo">1</div></flexbox-item>
  <flexbox-item><div class="flex-demo">2</div></flexbox-item>
</flexbox>
<divider>Vertical</divider>
<flexbox orient="vertical" :margin-left=0>
  <flexbox-item><div class="flex-demo" style="margin-left:0">1</div></flexbox-item>
  <flexbox-item><div class="flex-demo" style="margin-left:0">2</div></flexbox-item>
</flexbox>
</template>

<style>
.flex-demo {
  text-align: center;
  color: #fff;
  background-color: #20b907;
  margin-bottom: 8px;
  border-radius: 4px;
  -webkit-background-clip: padding-box;
}
</style>
```
### 嵌套布局

> 国内电商网站和支付应用最常见

> 1像素边框实现请参考1px解决方案

{% vux height=240,width='100%',components='Flexbox,FlexboxItem' %}
<template>
<flexbox :margin-left=0 style="height: 200px; background-color: #fff;" class="ui-border-tb ui-border-l ui-border-r">
  <flexbox-item class="ui-border-r"></flexbox-item>
  <flexbox-item>
    <flexbox orient="vertical" :margin-left=0>
      <flexbox-item class="ui-border-b"></flexbox-item>
      <flexbox-item style="height: 100px;"><!--height: 100% doesnot work here-->
        <flexbox :margin-left=0>
          <flexbox-item class="ui-border-r"></flexbox-item>
          <flexbox-item></flexbox-item>
        </flexbox>
      </flexbox-item>
    </flexbox>
  </flexbox-item>
</flexbox>
</template>
{% endvux%}