# Loading

## Props

| 参数         | 类型                 | 默认       | 说明 |
| ----------- | ---------------------- | ---------- | ------- |
| show  | Boolean | false | 是否显示，`双向绑定` |
| text | String or DOM  | Loading | 提示文字，与默认slot作用一致 |


## Slots

| 名字         | 说明            | 
| ----------- | --------------- | 
| 默认slot | 提示文字，因和text属性功能一致，因此可以二选一 |


## Demo


``` vux height=450 components=Loading,Group,Switch
<template>
<div>
  <group>
    <switch title="Toggle" :value.sync="show" @on-change="delayHide"></switch>
  </group>
  <loading :show="show" :text="text1"></loading>
</div>
</template>

<script>
export default {
  methods: {
    delayHide () {
      setTimeout(() => {
        this.show = false
      }, 5000)
    }
  },
  data () {
    return {
      show: false,
      text1: 'Hello world'
    }
  }
}
</script>
```