# Popup弹出层

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| show | 是否显示Popup，需要双向绑定 | Boolean | false |
| height | 弹出层高度 | String | auto |

> 如果希望弹出层铺满整个屏幕，则可设置`height=100%`

## Demo

``` vux height=400 width=100% components=Popup,Group,Switch

<template>
<div>
  <group>
    <switch title="Default popup" :value.sync="show"></switch>
    <switch title="Full popup" :value.sync="show1"></switch>
  </group>
  <popup :show.sync="show">
    <div class="popup0">
      <group>
        <switch title="Another Switcher" :value.sync="show"></switch>
      </group>
    </div>
  </popup>

  <popup :show.sync="show1" height="100%">
    <div class="popup1">
      <group>
        <switch title="Another Switcher" :value.sync="show1"></switch>
      </group>
    </div>
  </popup>
</div>
</template>
<script>
export default {
	data () {
		return {
			show: false,
			show1: false
		}
	}
}
</script>
<style>
.popup0 {
  padding-bottom:15px;
  height:200px;
}
.popup1 {
  width:100%;
  height:100%;
}
</style>
```
