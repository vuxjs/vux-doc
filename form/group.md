# Group

`Group`是一个特殊的表单`wrapper`组件，主要用于将表单分组，单个表单元素也算一组。所以常见的`行内`组件都`必须`作为`Group`的子组件。


包括：

+ Cell
+ XInput
+ XTextarea
+ Switch
+ Calendar
+ XNumber
+ Radio
+ Address
+ Datetime
+ Selector

## Props

| 参数         | 类型                  | 默认      | 说明 |
| ----------- | ---------------------- | ---------- | ------- |
| title | String | 无 | 分组标题 |
| title-color | String | 默认颜色 | -- |

## Demo

``` vux height=500 components=Group,Switch,Cell,XInput,XTextarea,Calendar,XNumber
<template>
<group title="I'm group title">
  <cell title="cell" value="hello world" is-link></cell>
  <x-input title="x-input"></x-input>
  <switch title="switch"></switch>
  <x-textarea placeholder="x-textarea"></x-textarea>
  <calendar title="Calendar"></calendar>
</group>

<group title="I'm another group title" title-color="green">
  <cell title="cell" value="hello world" is-link></cell>
  <x-input title="x-input"></x-input>
  <x-number title="x-number"></x-number>
</group>
</template>
```