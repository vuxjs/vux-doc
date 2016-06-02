# Cell

## Props

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| title | 可选，label文字 | String | 无 |
| value | 可选，右边文字 | String | 无 |
| inline-desc | 可选，label第二行文字 | String | 无 |
| link | 可选,支持http绝对路径及`v-link`配置 | String or Object | 无 |
| is-link | 可选，是否为链接，如果为true，样式上会出现箭头。当link存在时，is-link会自动设置为`true`  | Boolean  | false |
| primary | 可选，可选值为title和content, 对应的div会加上weui_cell_primary类名实现内容宽度自适应 | String | title |

## Slots

|    名字    | 说明                  | 
| ----------- | ------------------- | 
| 默认slot | value区域 |
| icon | title前，用于定义icon区域 |
| after-title | title 后面区域 |
| value | value区域, 同默认slot, 保留仅出于兼容考虑，不建议再使用 |

### Demo

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