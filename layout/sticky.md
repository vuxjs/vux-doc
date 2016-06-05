# Sticky 自动固定在顶部

> 如果你在使用Chrome开发过程中发现并没有按预期起到作用，不要慌，这是正常现象！具体请参考[#246](https://github.com/airyland/vux/issues/246)

## Demo

> 请打开新窗口查看效果

``` vux width=100% height=400 components=Sticky,Tab,TabItem

<template>
<br v-for="i in 8">
<sticky>
	<tab :line-width=1>
	  <tab-item selected>正在正映</tab-item>
	  <tab-item>即将上映</tab-item>
	</tab>
</sticky>
<br v-for="i in 50">
</template>
```
