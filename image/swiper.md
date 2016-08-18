# swiper

> swiper提供了`list`快捷设置和`swiper-item`子组件方便定义。

## Props


| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| list | 列表数据 | Array | 无 |
| direction | 方向 | String |　horizontal |
| show-dots | 是否显示indicator,只在list快捷形式下显示 | Boolean | true |
| show-desc-mask | 是否显示描述梦曾 | Boolean | true | 
| dots-position | indicator位置 | String | right |
| dots-class | indicator的附加样式类 | String | 无 |
| auto | 是否自动播放 | Boolean | false |
| loop | 是否循环播放 | Boolean | 无 |
| aspect-ratio | 纵横比,设置则自动根据宽度计算高度 | Number | 无 |
| min-moving-distance | 最小滑动距离 | Number | 0 |
| index | 指定显示item的 | Number | 0 | 
| interval | 轮播时间间隔 | Number | 3000 |
| threshold | 滑动距离阀值，当按住屏幕滑动超过此距离，松开手时，自动滑，否则不滑动 | Number | 50 |
| duration | 滑屏动画时间，单位ms，数值越小，滑动越快 | Number | 300 |
| height | 容器高度 | String | auto |

## 示例

### 基本使用

``` vux height=200 components=Swiper
<template>
<div>
  <swiper :list="list" auto></swiper>
<div>
</template>

<script>
export default {
  data: function () {
    return {
      list: [{
        url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400385458&ampidx=1&ampsn=78f6b8d99715384bdcc7746596d88359&ampscene=19#wechat_redirect',
        img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/1.jpg',
        title: '如何手制一份秋意的茶？'
      }, {
        url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400160890&ampidx=1&ampsn=29ef02af25793a11a3f6aec92bfb46c1&ampscene=19#wechat_redirect',
        img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/2.jpg',
        title: '茶包VS原叶茶'
      }, {
        url: 'http://mp.weixin.qq.com/s?__biz=MzAxNjU0MDYxMg==&ampmid=400094682&ampidx=1&ampsn=8231a2053b772b2108784fccc254d28c&ampscene=19#wechat_redirect',
        img: 'http://7xqzw4.com2.z0.glb.qiniucdn.com/3.jpg',
        title: '播下茶籽，明春可发芽？'
      }]
    }
  }
}
</script>
```
