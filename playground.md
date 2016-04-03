# playground

## 页面接口

### https://vux.li/api/v1/demo.html

> 简易接口，用于把代码拼凑成完整的vue页面，文档中的例子都是使用该接口以iframe嵌入

### url参数

+ `components` 使用的组件，英文逗号分隔，如 `Group,Radio`
+ `javascript` js代码，以`export default {`开头， `}`结束
+ `template` 模板，普通`html`代码
+ `style` 样式,只支持一般css，不支持指定`lang`及`scoped`


## 在文档中的例子：

> 注意的是 Gitbook会渲染双花括号,因此所有的花括号用`<<>>`代替，render时会自动替代成正确的。

``` html
<span> {{arg}} </span>
=>
<span> <<arg>> </span>
```

``` html
// demo写法和 vue 文件一致，使用template, script, style标签。
// vux区域的with指定宽度，默认为100%,height指定高度，components指定使用到的组件名字

{% vux width=100,height=50,components="Tab,TabItem" %} 
<template>
<tab>
  <tab-item :selected="demo1 === '已发货'" @click="demo1 = '已发货'">已发货</tab-item>
  <tab-item :selected="demo1 === '未发货'" @click="demo1 = '未发货'">未发货</tab-item>
  <tab-item :selected="demo1 === '全部订单'" @click="demo1 = '全部订单'">全部订单</tab-item>
</tab>
</template>

<script>
export default {
  data: {
    demo1: '未发货'
  }
}
</script>

<style>
.selector {
  color: red;
}
</style>
{% endvux %}
```