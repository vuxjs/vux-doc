# Actionsheet

## 属性

| 参数        | 类型        | 默认值 | 说明 |
| ----------- | ---------------------- | ---------- | ------- |
| show | Boolean | false | 显示绑定值，双向绑定 |
| show-cancel | Boolean | false | 是否显示取消按钮 |
| menus  | Object | {} |  菜单列表，格式见下|
| cancelText | String | cancel | 取消按钮文字 |

> menus格式如下

``` js
{
  menu1: 'Take Photo',
  menu2: 'Choose from photos'
}
```

## 事件
| 事件名       | 参数       | 说明 |
| ----------- | ---------------------- | ---------- |
| on-menu-click | (menuKey, menuValue) | 点击菜单时触发 | 
| on-cancel | -- | 点击取消时触发 |


## Demo

``` vux height=400 components=Group,Switch,Actionsheet
<template>
<div>
  <group>
    <switch title="show actionsheet1" :value.sync="show1"></switch>
    <switch title="show actionsheet2" :value.sync="show2"></switch>
    <switch title="show actionsheet3" :value.sync="show3"></switch>
  </group>
  <actionsheet :show.sync="show1" :menus="menus1"></actionsheet>
  <!-- 显示取消按钮 -->
  <actionsheet :show.sync="show2" :menus="menus2" show-cancel></actionsheet>
  <!-- 菜单响应 -->
  <actionsheet :show.sync="show3" :menus="menus3" @menu-click="click" show-cancel @cancel-text="取消"></actionsheet>
</div>
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
