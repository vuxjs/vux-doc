# vue项目

> `vue-cli`的使用请查看[文档][https://github.com/vuejs/vue-cli]

> `vue-loader`[文档](http://vuejs.github.io/vue-loader/)

``` bash
# 安装 vue-cli
npm install -g vue-cli

# 初始化 webpack 项目
vue init webpack my-project
cd my-project
# npm可能出现访问速度极慢的情况，推荐使用cnpm
npm install
#安装 vux 
npm install vux
# 开发版安装请使用 npm install vux@next
# 调试
npm run dev
```


```` html
<template>
  <div>
    <group>
      <cell title="vue" value="cool"></cell>
    </group>
  </div>
</template>

<script>
// 不推荐的方式，会打包所有vux模块
import { Group, Cell } from 'vux'

// 推荐的方式，按需加载需要的组件
import Group from 'vux/dist/components/group'
import Cell from 'vux/dist/components/cell'

export default {
  components: {
    Group,
    Cell
  }
}
</script>

<style>
@import '~vux/dist/vux.css';
</style>
````
