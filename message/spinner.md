# Spinner

## Props

# 文档模板

## Props

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| type | String | ios | 类型,可选值有 'android', 'ios', 'ios-small', 'bubbles', 'circles', 'crescent', 'dots', 'lines', 'ripple', 'spiral' |


## Demos

``` vux height=500 components=Group,Cell,Spinner
<template>
<div>
  <group>
    <cell v-for="type in types" :title="type">
      <spinner :type="type"></spinner>
    </cell>
  </group>
</div>
</template>

<script>
export default {
  data () {
    return {
      types: ['android', 'ios', 'ios-small', 'bubbles', 'circles', 'crescent', 'dots', 'lines', 'ripple', 'spiral']
    }
  }
}
</script>
```