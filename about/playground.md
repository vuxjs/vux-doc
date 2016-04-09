# playground

## 页面接口

### https://vux.li/api/v1/demo.html

> 简易接口，用于把代码拼凑成完整的vue页面，文档中的例子都是使用该接口以iframe嵌入。

> 注意`GET`方式url长度有限制，所以这种方式用于相对简单的例子。

### url参数

+ `components` 使用的组件，英文逗号分隔，如 `Group,Radio`
+ `javascript` js代码，以`export default {`开头， `}`结束
+ `template` 模板，普通`html`代码
+ `style` 样式,只支持一般css，不支持指定`lang`及`scoped`


## 在文档中的例子：

写法同`vue`文件，但是只支持普通css写法，不支持less等。不支持`import`外部组件。

> 通过components来注册使用到的组件，`必需`

> 宽度width默认为100%

> 高度height默认为 100

```` html
``` vux width=100% height=100 components=Circle raw=true
<template>
  <div style='width:100px;height:100px;'>
    <circle :percent='percent2' :stroke-width=6 :trail-width=6 :stroke-color='strokeColor2' trail-color="#ececec">
      <span :style="{color: strokeColor2}">{{percent2}}%</span>
    </circle>
  </div>
</template>

<script>
export default {
  ready () {
    setInterval(this.update, 2000)
  },
  data () {
    return {
      percent2: 30,
      strokeColor2: '#3FC7FA'
    }
  },
  methods: {
    update: function () {
      const colorMap = ['#3FC7FA', '#85D262', '#FE8C6A']
      this.percent2 = parseInt(Math.random() * 100, 10)
      this.strokeColor2 = colorMap[parseInt(Math.random() * 3, 10)]
    }
  }
}
</script>

<style>
.hello {


}
</style>
```
````

### 渲染结果

``` vux width=100% height=100 components=Circle
<template>
<div style='width:100px;height:100px;'>
  <circle :percent='percent2' :stroke-width=6 :trail-width=6 :stroke-color='strokeColor2' trail-color="#ececec">
    <span :style="{color: strokeColor2}">{{percent2}}%</span>
  </circle>
</div>
</template>

<script>
export default {
  ready () {
    setInterval(this.update, 2000)
  },
  data () {
    return {
      percent2: 30,
      strokeColor2: '#3FC7FA'
    }
  },
  methods: {
    update: function () {
      const colorMap = ['#3FC7FA', '#85D262', '#FE8C6A']
      this.percent2 = parseInt(Math.random() * 100, 10)
      this.strokeColor2 = colorMap[parseInt(Math.random() * 3, 10)]
    }
  }
}
</script>

<style>
.hello {
}
</style>
```