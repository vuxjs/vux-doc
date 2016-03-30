# playground

## 接口

### /api/v1/demo-by-code.html

> 简易接口，用于把代码拼凑起来

+ `components` 使用的组件
+ `javascript` js代码
+ `template` 模板
+ `style` 样式

### /v1/gist/:id

> 根据代码生成的页面链接，方便以iframe的方式插入页面

代码和vue文件基本一致，但是增加了`<components></components>`定义调用的组件

``` html
<template>
</template>

<style>
</style>

<components>
Radio, Switch, Input
</components>

<script>
</script>
```