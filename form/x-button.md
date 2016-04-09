# x-button 按钮

## API

> 按钮文字可以用text属性也可以用直接用默认slot

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| type | 可选，可选值为default,primary,warn | String | default |
| disabled | 可选，是否disabled | Boolean | false |
| 默认slot | 可选，按钮文字 | DOM | 无 |
| text | 可选，按钮文字 | String | 无 |


### 一般使用

``` vux components=XButton height=170
<template>
<x-button>submit</x-button>
<x-button type="primary">primary</x-button>
<x-button type="warn">Delete</x-button>
</template>
```

### 不可点击

``` vux components=XButton height=170
<template>
<x-button disabled>submit</x-button>
<x-button type="primary" disabled>primary</x-button>
<x-button type="warn" disabled>Delete</x-button>
</template>
```

### 直接用:text指定按钮文字

``` vux components=XButton height=50
<template>
<x-button type="primary" :text="btnText" :disabled="isDisabled" @click="click"></x-button>
</template>

<script>
export default {
  data: {
    btnText: 'click me',
    isDisabled: false
  },
  methods: {
    click: function () {
      const _this = this
      this.isDisabled = true
      this.btnText = 'Processing'
      setTimeout(function () {
        _this.btnText = 'Done'
      }, 2000)
    }
  }
}
</script>
```