# x-header

> 目前x-header并不处理定位，请手动用class或者style设置。

## Props

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| leftOptions.showBack | Boolean  | true | 是否显示返回箭头 |
| leftOptions.backText | String | Back | 返回文字，可以为空 |
| leftOptions.preventGoBack | Boolean | false | 是否阻止点击Back时的后退，默认会调用`history.back()` |
| rightOptions.showMore | Boolean | false | 是否显示更多图标 |


## Events


| 名字 | 参数  | 描述 |
|-----|-----|-----|
| on-click-back | - | 点击后退按钮或者文字时触发, 并且只有leftOptions.preventGoBack设为true时才触发 |
| on-click-more | - | 点击更多图标时触发 |


## Slots


| 名字  | 描述 |
|-----|-----|
| 默认slot | 标题文字 |
| left | 位于Back之后的内容 |
| right | 位于showMore之后的内容 |


## Demos

``` vux height=570 components=XHeader,Divider
<template>
<divider>默认</divider>
<x-header>This is the page title.</x-header>
<divider>不显示后退</divider>
<x-header :left-options="{showBack: false}">do not show Back</x-header>
<divider>显示右侧更多</divider>
<x-header :right-options="{showMore: true}">with more menu</x-header>
<divider>使用 right 插槽</divider>
<x-header>with right link<a slot="right">Feedback</a></x-header>
<divider>自动文字截断</divider>
<x-header>long long long long long long long ong long long long long long long text<a slot="right">Feedback</a></x-header>
<divider>使用 left 插槽</divider>
<x-header>with left slot<a slot="left">Close</a></x-header>
<divider>更改背景颜色</divider>
<x-header style="background-color:#000;">custom background color</x-header>
</template>
```