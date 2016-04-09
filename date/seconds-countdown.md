# 秒数倒计时

## 使用场景

> 用于发送短信等耗费操作时，不要依赖前端验证，`必须一定要`同时在后端进行ratelimit验证。

+ 短信验证重发的场景中。一般为60s, 120s

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| time| 可选，计时秒数  | Number  | 60 |
| start| 可选，默认自动倒计时，设为false时可以手动开始计时 | Boolean | true |

## Demo

``` vux height=65 components=Group,Cell,Countdown
<template>
<group>
  <cell title="15s" :value="value">
    <countdown slot="value" :time="15" @on-finish="finish" v-show="show"></countdown>
  </cell>
</group>
</template>

<script>
export default {
  methods: {
    finish: function (index) {
      this.show = false
      this.value = 'completed'
      console.log('current index', index)
    }
  },
  data () {
    return {
      show: true,
      value: ''
    }
  }
}
</script>
```

``` vux height=125 components=Group,Cell,Countdown,Switch
<template>
<group>
  <switch title="start" :value.sync="start"></switch>
  <cell title="15s">
    <countdown slot="value" :time="time" :start="start" @on-finish="finish"></countdown>
  </cell>
</group>
</template>

<script>
export default {
  methods: {
    finish: function (index) {
      this.start = false
      this.time = 20
    }
  },
  data () {
    return {
      time: 15,
      start: false
    }
  }
}
</script>
```
