# checker 灵活的单选组件

虽然有`Radio`组件提供单选功能，但是有很多情况下我们需要定义选项的样式布局，比如电商网站的商品属性选择。因此提供了`checker`。

> 当前组件由 `checker` 和 `checker-item` 组成

## checker 属性

| 参数         | 说明                  | 类型        | 
| ----------- | ---------------------- | ---------- | 
| default-item-class | 可选，应用于所有子选项 | String | 
| selected-item-class | 必选，选中时的class | String |
| disabled-item-class | 当有`不可点击`的选项时必选 | String | 
| value | 必选，双向绑定 | String |
| on-change | 选中值变化时触发 | 参数为`(value)` | 
| on-item-click | 当点击任何选项时触发 | 参数为`(itemValue, isDisabled)` |

## checker-item 属性

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| value | 必选，选项值 | String | |
| disabled | 可选，是否不可点击 | Boolean | false |

## 使用

``` html
<checker :value.sync="somevalue"
         default-item-class="demo-item-defalut"
         selected-item-class="demo-item-selected">
  <checker-item value="1">1</checker-item>
  <checker-item value="2">2</checker-item>
  <checker-item value="3" disabled>3</checker-item>
</checker>
```

## 例子

