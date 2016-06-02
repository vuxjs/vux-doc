# x-number 数字输入组件

> `x-number`需要与`group`配合使用。

## Props

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| title | 可选，标题 | String | 无 |
| value | 当前输入框值 | Number | 0 |
| min | 可选，数字范围最小值 | Number | 无 |
| max | 可选，数字范围最大值 | Number | 无 |
| step| 可选，步长 | Number | 1 |
| fillable | 可选，是否可以输入 | Boolean | true |
| width | 可选，输入框宽度 | Number | 50 |


## Events


| 名字 | 参数  | 描述 |
|-----|-----|-----|
| on-change | value | 值变化时触发 |


## 示例

### 基本使用

``` vux width=100% height=100px components=Group,XNumber

<template>
<group>
  <x-number title="Number" :value=0 :min=0 :max=10 @change="change"></x-number>
</group>
</template>
<script>
export default {
  methods: {
    change: function (val) {
      console.log('change', val)
    }
  }
}
</script>
```

### 自定义步长

``` vux height=150px components=Group,XNumber
<template>
<group title="set step=0.5">
  <x-number title="Number" :step=0.5></x-number>
</group>
</template>
```

### 禁止键盘输入

``` vux height=150px components=Group,XNumber

<template>
<group title="fillable = false">
  <x-number :value=10 title="Number" :fillable=false></x-number>
</group>
</template>

```

### 和其他组件共用

``` vux height=200px components=Switch,Group,XNumber

<template>
<group title='with other element'>
  <x-number title="Number" :min=-5 :max=8 :value=1 type="inline"></x-number>
  <x-number title="Number" :min=-5 :max=8 :value=1 type="inline"></x-number>
  <switch title="Other element" :value=true></switch>
</group>
</template>
```