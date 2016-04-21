# Shake 摇一摇

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| stop| 是否停止派发摇动事件  | Boolean  | false |
| threshold| 可选，摇动力度阈值  | Number  | 15 |
| timeout| 可选，事件收集频率  | Number  | 1000 |


## Demo

``` vux height=200 components=Shake,XButton
<template>
<div>
  <p style="text-align:center">shake your phone</p>
  <p><x-button text="停止接收摇动事件" type="primary" @click="stopShake = false"></x-button></p>
  <shake @shake="shake" :threshold=5></shake>
</div>
</template>
<script>
export default {
  data () {
    return {
      stopShake: false
    }
  },
  methods: {
    'on-shake': function () {
      alert('shaked')
    }
  }
}
</script>
```
