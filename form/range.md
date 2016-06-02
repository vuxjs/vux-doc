# Range 组件

## Props

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| decimal | 可选，是否开启小数支持 | Boolean | false |
| value | 可选，当前选择值 | Number | 0 |
| min | 可选，取值范围最小值 | Number | 0 |
| max | 可选，取值范围最大值 | Number | 100 |
| min-html | 可选，最小值定制内容 | String | 无 |
| max-html | 可选，最大值定制内容 | String | 无 |
| step | 可选，滑动步长 | Number | 0 |
| disabled | 可选，是否为禁止状态 | Boolean | false |
| disabled-opacity | 可选，禁止状态下控件的透明度 | Number | 0.75 |
| range-bar-height | 可选，状态条的高度 | Number | 1 |
| range-handle-height | 可选，滑柄位置 | Number | 30 |


## Demo

### 基本使用

``` vux width=100% height=220px components=Group,Cell,Range

<template>
<group>
  <cell title="Default" :inline-desc="'value: '+value1" primary="content">
    <range slot="value" :value.sync="value1"></range>
  </cell>
  <cell title="allow decimals" :inline-desc="'value is: '+value2" primary="content">
    <range slot="value" :value.sync="value2" decimal></range>
  </cell>
  <cell title="value=20" :inline-desc="'value is: '+value3" primary="content">
    <range slot="value" :value.sync="value3"></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value1: 0,
      value2: 0,
      value3: 20
    }
  }
}
</script>
```

### 设置起始值和最大值

``` vux width=100% height=210px components=Group,Cell,Range

<template>
<group>
  <cell title="min=8" :inline-desc="'value is: '+value1" primary="content">
    <range slot="value" :value.sync="value1" :min=8></range>
  </cell>
  <cell title="max=88" :inline-desc="'value is: '+value2" primary="content">
    <range slot="value" :value.sync="value2" :max=88></range>
  </cell>
  <cell title="min and max" :inline-desc="'value is: '+value3" primary="content">
    <range slot="value" :value.sync="value3" :min=7 :max=77></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value1: 25,
      value2: 25,
      value3: 25
    }
  }
}
</script>
```

### 自定义步长

``` vux width=100% height=100px components=Group,Cell,Range
<template>
<group>
  <cell title="step=10" :inline-desc="'valus is: '+value" primary="content">
    <range slot="value" :value.sync="value" :min=7 :max=77 :step=10></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value: 25
    }
  }
}
</script>
```

### 禁用组件

``` vux width=100% height=150px components=Group,Cell,Range

<template>
  <group>
    <cell title="disabled=true" :inline-desc="'valus is: '+value1" primary="content">
      <range slot="value" :value.sync="value1" disabled></range>
    </cell>
    <cell title="Opacity" :inline-desc="'valus is: '+value2" primary="content">
      <range slot="value" :value.sync="value2" disabled :disabled-opacity=0.1></range>
    </cell>
  </group>
</template>
<script>
export default {
  data () {
    return {
      value1: 25,
      value2: 25
    }
  }
}
</script>
```

### 设置bar的高度和手柄的位置

``` vux width=100% height=150px components=Group,Cell,Range

<template>
<group>
  <cell title="Bar height" :inline-desc="'value is: '+value" primary="content">
    <range slot="value" :value.sync="value" :range-bar-height=4></range>
  </cell>
  <cell title="Handle position" :inline-desc="'value is: '+value" primary="content">
    <range slot="value" :value.sync="value" :range-handle-height=5></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value: 25
    }
  }
}
</script>
```

### 自定义初始值和最大值

``` vux width=100% height=150px components=Group,Cell,Range

<template>
<group>
  <cell title="文字大小" :inline-desc="'font size: ' + value1" primary="content">
    <range slot="value" :value.sync="value1" :min="12" :max="22" min-HTML="<span style='font-size:12px;'>小</span>" max-HTML="<span style='font-size:22px;'>大</span>"></range>
  </cell>
  <cell title="bcontentness" :inline-desc="'value is: ' + value2 + '%'" primary="content">
    <range slot="value" :value.sync="value2" min-HTML="<span style='font-size:16px;color:#F90;'>☼</span>" max-HTML="<span style='font-size:30px;color:#F90;'>☼</span>"></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value1: 14,
      value2: 25
    }
  }
}
</script>
```

### 双向绑定

``` vux width=100% height=150px components=Group,Cell,Range

<template>
<group>
  <cell title="Default" :inline-desc="'value: '+value" primary="content">
    <range slot="value" :value.sync="value"></range>
  </cell>
  <cell title="Default" :inline-desc="'value: '+value" primary="content">
    <range slot="value" :value.sync="value"></range>
  </cell>
</group>
</template>
<script>
export default {
  data () {
    return {
      value: 0
    }
  }
}
</script>
```