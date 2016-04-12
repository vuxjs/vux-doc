# Radio 单选

>  `Radio`必须和`Group`一起使用。

## 属性

+ options Array 选项列表,非空
+ value 值，双向绑定
+ fillMode Boolean,是否增加自定义输入框
+ fillPlaceholder String,自定义输入框的提示
+ fillLable String,自定义输入框标签

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
