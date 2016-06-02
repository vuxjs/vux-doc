# 背景模糊

## 场景

背景模糊常用于个人中心的头像背景, 音乐播放界面的背景。

## Props

| 名字 | 类型 | 默认 | 描述 |
|-----|-----|-----|-----|
| url | String | 无 | 图片地址 |
| height | Number | 200 | 高度 |
| blur-amount| Number | 10 | 模糊程度 |


## Slots


| 名字  | 描述 |
|-----|-----|
| 默认slot | 图片上面内容 |


## 示例

### 纯背景

``` vux height=200 components=Blur
<style></style>
<template>
<blur :blur-amount=40 url="https://o3e85j0cv.qnssl.com/tulips-1083572__340.jpg"></blur>
</template>
```

### 背景上添加内容

> 通过默认slot支持

``` vux height=200 components=Blur
<template>
<blur :blur-amount=40 url="https://o3e85j0cv.qnssl.com/hot-chocolate-1068703__340.jpg">
  <p class="center">
    <img src="https://o3e85j0cv.qnssl.com/hot-chocolate-1068703__340.jpg">
  </p>
</blur>
</template>

<style>
.center {
  text-align: center;
  padding-top: 20px;
  color: #fff;
  font-size: 18px;
}
.center img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  border: 2px solid #ececec;
}
</style>
```
