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
#安装 vux 发版请使用 npm install vux@next
npm install vux
#安装less-loader
npm install less-loader --save-dev
# 调试
npm run dev
```


## 在webpack.base.conf.js添加loader

``` javascript
{
  test: /vux.src.*?js$/,
  loader: 'babel'
}
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
import Group from 'vux/src/components/group'
import Cell from 'vux/src/components/cell'

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

> 可以配置alias使用更简短的引用路径

``` javascript
resolve: {
  alias: {
    'vux-components': 'vux/src/components/'
  }
}
```

> 那么就可以这样引用

``` javascript
import Group from 'vux-components/group'
import Cell from 'vux-components/cell'
```
