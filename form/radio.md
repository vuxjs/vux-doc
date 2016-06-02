# Radio 单选

>  `Radio`必须和`Group`一起使用。

## Props

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| options | Array | 无 | 选项列表, 支持简单数组及key=>value键值对，使用键值对时表单值为key |
| value | String | 无 | 表单值，必选，双向绑定 |
| fill-mode | Boolean | false | 是否增加自定义输入框 |
| fill-placeholder | String | 无 |自定义输入框的提示 |
| fill-lable | String | 无 | 自定义输入框标签 |

## Events


| 名字 | 参数  | 描述 |
|-----|-----|-----|
| on-change | value | 值变化时触发 |


## 预设值

``` vux height=140 components=Radio,Group
<template>
<group>
    <radio :options="options" value="China"></radio>
</group>
</template>

<script>
export default {
    data () {
        return {
            options:['China','Japan']
        }
    }
}    
</script>
```

## 自定义输入框

``` vux height=200 components=Radio,Group
<template>
<group>
    <radio :options="options" fill-mode fill-label="Other" fill-placeholder="填写其他的哦"></radio>
</group>
</template>

<script>
export default {
    data () {
        return {
            options:['China','Japan']
        }
    }
}
</script>
```

## 数据双向绑定

``` vux height=300 components=Radio,Group
<template>
<group title="radio1">
    <radio :options="options" :value.sync="value"></radio>
</group>
<group title="radio2">
    <radio :options="options" :value.sync="value"></radio>
</group>
</template>

<script>
export default {
    data () {
        return {
            options:['China','Japan'],
            value:'China'
        }
    }
}
</script>
```

## change事件

``` vux height=200 components=Radio,Group
<template>
<group>
    <radio :options="options" @change="change"></radio>
</group>
</template>

<script>
export default {
    data () {
        return {
            options:['China','Japan']
        }
    },
    methods: {
        change (val) {
            console.log('change',val)
        }
    }
}
</script>
```
