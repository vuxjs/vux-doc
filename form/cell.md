# Cell

> cell不处理具体的跳转链接，`is-link`仅用来设置样式，如果使用`vue-router`可以在上面直接使用`v-link`

> 如果没有使用`vue-router`，那么可以直接用`@click`事件要处理跳转

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| title | 可选，label文字 | String | 无 |
| value | 可选，右边文字 | String | 无 |
| inline-desc | 可选，label第二行文字 | String | 无 |
| is-link | 可选，是否为链接，如果为true，样式上会出现箭头  | Boolean  | false |
| primary | 可选，可选值为title和content, 对应的div会加上weui_cell_primary类名实现内容宽度自适应 | String | title |

## slot

+ icon label文字前，用于定义icon区域
+ after-title 文字后
+ value value区域

### 文字

``` vux height=65 components=Group,Cell
<template>
<group>
  <cell title="My Account" value="Protected" @click="click"></cell>
</group>
</template>
<script>
export default {
  methods: {
    click: function () {
      alert('click')
    }
  }
}
</script>
```
### 链接

``` vux height=65 components=Group,Cell
<template>
<group>
  <cell title="My Account" value="Protected" is-link></cell>
</group>
</template>
```