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

``` vux components=Checker,CheckerItem
<template>
<checker :value.sync="demo1" default-item-class="demo1-item" selected-item-class="demo1-item-selected">
  <checker-item value="1">1</checker-item>
  <checker-item value="2">2</checker-item>
  <checker-item value="3">3</checker-item>
</checker>
<br/>
<span>current value is: {{demo1}}</span>
</template>

<script>
export default {
  data () {
    return {
      demo1: ''
    }
  }
}
</script>

<style>
.demo1-item {
  display: inline-block;
  border: 1px solid #ececec;
  padding: 5px 15px;
}
.demo1-item-selected {
  border: 1px solid green;
}
</style>
```

### 默认值

``` vux components=Checker,CheckerItem
<template>
<checker :value.sync="demo2" default-item-class="demo2-item" selected-item-class="demo2-item-selected">
  <checker-item value="1">1</checker-item>
  <checker-item value="2">2</checker-item>
  <checker-item value="3">3</checker-item>
</checker>
<br/>
<span>current value is: {{demo2}}</span>
</template>

<script>
export default {
  data () {
    return {
      demo2: '2'
    }
  }
}
</script>

<style>
.demo2-item {
  width: 40px;
  height: 40px;
  border: 1px solid #ccc;
  display: inline-block;
  border-radius: 50%;
  line-height: 40px;
  text-align: center;
}
.demo2-item-selected {
  border-color: green;
}
</style>
```

### disabled

``` vux height=400 components=Checker,CheckerItem,Group,Cell,Popup
<template>
<group>
  <cell title="select color" :value="demo4" is-link @click="showPopup=true"></cell>
</group>
<popup :show.sync="showPopup" class="checker-popup">
  <div style="padding:10px 10px 40px 10px;">
    <p style="padding: 5px 5px 5px 2px;color:#888;">Colors</p>
    <checker
    :value.sync="demo4"
    default-item-class="demo4-item"
    selected-item-class="demo4-item-selected"
    disabled-item-class="demo4-item-disabled"
    @on-item-click="showPopup=false">
      <checker-item value="花跟叶">花跟叶</checker-item>
      <checker-item value="鸟与树">鸟与树</checker-item>
      <checker-item value="我和你">我和你</checker-item>
      <checker-item value="全套礼品装" disabled>全套礼品装</checker-item>
    </checker>
  </div>
</popup>
</template>

<script>
export default {
  data () {
    return {
      demo4: '花跟叶',
      showPopup: false
    }
  }
}
</script>

<style>
.demo4-item {
  display: inline-block;
  background-color: #ddd;
  color: #222;
  font-size: 14px;
  padding: 5px 10px;
  margin-right: 10px;
  line-height: 18px;
  border-radius: 15px;
}
.demo4-item-selected {
  background-color: #FF3B3B;
  color: #fff;
}
.demo4-item-disabled {
  color: #999;
}
</style>
```