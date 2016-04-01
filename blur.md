# 背影模糊

## 场景

背景模糊常用于个人中心的头像背景。

## 示例

{% vux height=200 %}
<components>Blur</components>
<style></style>
<template>
<blur :blur-amount=40 url="https://o3e85j0cv.qnssl.com/tulips-1083572__340.jpg"></blur>
</template>
{% endvux %}

### 背景上添加内容

> 通过默认slot支持

{% vux height=200 %}
<components>Blur</components>

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
{% endvux %}

