# Confirm 

## 使用场景

confirm用于需要用户确认操作的情况。

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| cancel-text | 可选，取消按钮文字 | String | cancel |
| confirm-text | 可选，确认按钮文字 | String | confirm |
| 默认slot | 可选，提示消息内容 | DOM | 无 |
| title | 必选，提示标题 | String | 无 |
| show | 必选，是否显示，`双向绑定` | Boolean | false |
| on-confirm | 确认事件 | 事件 | 无 |
| on-cancel | 取消事件 | 事件 | 无 |

> 事件名字从`0.0.105`后从`confirm`和`cancel`重命名为`on-confirm`和`on-cancel`

## Demo

### 默认按钮文字

``` vux height=200 components=Confirm,Group,Switch
<template>
<group>
  <switch title="Toggle" :value.sync="show"></switch>
</group>
<confirm :show.sync="show" title="confirm deleting the item"><p style="text-align:center;">Are you sure?</p></confirm>
</template>

<script>
export default {
  data () {
    return {
      show: false
    }
  }
}
</script>
```

### 监听事件

``` vux height=200 components=Confirm,Group,Switch
<template>
<group>
  <switch title="Toggle" :value.sync="show"></switch>
</group>
<confirm :show.sync="show" confirm-text="确定" cancel-text="取消" title="操作提示" @on-confirm="onAction('确认')" @on-cancel="onAction('取消')">
  <p style="text-align:center;">操作不可撤消哦?</p>
</confirm>
</template>

<script>
export default {
  methods: {
    onAction: function (type) {
      alert(type)
    }
  },
  data () {
    return {
      show: false
    }
  }
}
</script>
```