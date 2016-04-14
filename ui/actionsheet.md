# Actionsheet 上拉菜单

## 属性

+ show 控制菜单显示，默认是false
+ menus 菜单内容，注意格式是键值对而非数组
+ show-cancel 是否显示取消按钮，默认是false

## demos

``` html
<template>
<button @click="show1=true">show actionsheet1</button>
<button @click="show2=true">show actionsheet2</button>
<button @click="show3=true">show actionsheet3</button>

<actionsheet :show.sync="show1" :menus="menus1"></actionsheet>
<!-- 显示取消按钮 -->
<actionsheet :show.sync="show2" :menus="menus2" show-cancel></actionsheet>
<!-- 菜单响应 -->
<actionsheet :show.sync="show3" :menus="menus3" @menu-click="click" show-cancel></actionsheet>
</template>

<script>
export default {
    data () {
        return {
            show1:false,
            menus1:{
                menu1: 'Share to friends',
                menu2: 'Share to timeline'
            },
            show2:false,
            menus2: {
                menu1: 'Take Photo',
                menu2: 'Choose from photos'
            },
            show3:false,
            menus3: {
                menu1: 'friends comment'
            }
        }
    },
    methods: {
        click (key) {
            console.log(key)
        }
    }
}
</script>
```