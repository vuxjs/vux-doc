# Flexbox

> 当前的flexbox仅实现了子元素水平和垂直平分。

### 简单平分
{% vux height=160 %}
<components>Divider,Flexbox,FlexboxItem</components>

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
  border-top-left-radius: 4px;
  border-top-right-radius: 4px;
  border-bottom-left-radius: 4px;
  border-bottom-right-radius: 4px;
  -webkit-background-clip: padding-box;
}
</style>
{% endvux %}

### 嵌套布局

> 国内电商网站和支付应用最常见

{% vux height=240 %}
<components>Divider,Flexbox,FlexboxItem</components>

<template>
<divider>Nested Flexbox</divider>
<flexbox :margin-left=0 style="height: 200px; background-color: #fff;" class="ui-border-tb">
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