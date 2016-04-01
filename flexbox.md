# Flexbox

> 当前的flexbox仅实现了子元素水平和垂直平分。

{% vux %}
<components>Divider,Flexbox,Flexbox-item</components>

<template>
<divider>Horizontal</divider>
<flexbox>
  <flexbox-item><div class="flex-demo">1</div></flexbox-item>
  <flexbox-item><div class="flex-demo">2</div></flexbox-item>
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

{% vux %}
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