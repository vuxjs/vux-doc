# Progress 进度条

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| template | 进度条模板编号 | Number | 0 |
| percent | 当前进度百分比 | Number | 0 |

### template


* `template=0`，默认值，使用weui提供的进度条样式进行展示。

* `template=1`，Determinate

[![](https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/determinate.gif)](https://github.com/lightningtgc/MProgress.js#types-and-preview)

* `template=2`，Buffer

[![](https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/buffer.gif)](https://github.com/lightningtgc/MProgress.js#types-and-preview)

* `template=3`，Indeterminate

[![](https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/indeterminate.gif)](https://github.com/lightningtgc/MProgress.js#types-and-preview)

* `template=4`，Query Indeterminate and Determinate

[![](https://raw.githubusercontent.com/lightningtgc/MProgress.js/gh-pages/styles/images/query.gif)](https://github.com/lightningtgc/MProgress.js#types-and-preview)


## Demo

``` vux height=300 components=Group,Progress
<template>
<div>
	<group title="默认">
		<progress></progress>
	</group>
	<group :title="'双向绑定: ' + percent1 + '%">
		<progress :percent.sync="percent1"></progress>
	</group>
  <group title="template=2, Buffer">
 		 <progress :template="2"></progress>
  </group>
  <group title="template=3, Indeterminate">
  		<progress :template="3"></progress>
  </group>
  <group title="template=4, Query Indeterminate and Determinate">
  		<progress :template="4"></progress>
  </group>
</div>
</template>
<script>
export default {
	data () {
		return {
			percent1: 50
		}
	}
}
</script>
```