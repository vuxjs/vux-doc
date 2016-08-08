# 常见问题

## 其他格式的文档有么?

+ [PDF](https://www.gitbook.com/download/pdf/book/vuxjs/vux)
+ [ePub](https://www.gitbook.com/download/epub/book/vuxjs/vux)
+ [Mobi](https://www.gitbook.com/download/mobi/book/vuxjs/vux)

## 不懂Vue， 怎么用

去学

## Vux是微信官方项目吗

不是，但是Vux依赖于微信官方开发的[`WeUI`](https://github.com/weui/weui)

## Vux和Vuex名字太像了

真不是故意的

## 可以在template中使用其他标签吗

当然可以，局部注册组件的时候指定名字。

``` js
{
  components: {
    xalert: Alert
  }
}

```

如果使用全局注册，则

``` js
Vue.component('xalert', vuxAlert)
```

## 为什么部分组件要加x-前缀

若不更名，可能在开发时与标准html标签相同而导致冲突或者bug。

## 有QQ交流群吗

没有。
但是你可以**付费**加入Bearychat。
Bearychat [vux@bearychat](https://vux.bearychat.com/)

### 为什么要付费：

> 目前处理起来很费时间

> 设定门槛

> 时间有限，无法用同样的标准来对待每一位用户的每一个问题，并且不同的用户对技术支持的需求和紧急程度不同。

- 大部分人加入后没有任何问题建议，这不是我希望看到的，对项目开发无益，而我还需要去审核这些无用的申请
- 一部分同学不熟悉Vue提的跟Vux没任何关系，回答无非帖个文档链接
- 一部分同学不会正确提问题，过滤这些问题浪费时间，即使我有空，一步一步沟通也浪费时间
- 一部分同学问的是Web相关的其他问题
- 可能有惊喜

### 不付费就提不了问题吗

不是，你依然可以到Github上提交Vux相关issue。付费只是提供了**有门槛但更为快速**的沟通方式，同时你也可以咨询其他问题。
但是Bearychat不是即时沟通，不能保证随问随回。

假如公司项目已经使用Vux，那么可以理解为支持开源项目以及获取更加快速的技术支持。

### 如何付费

扫下面支付码支付 **￥188**，然后把支付码写在加入申请信息中。

### 满足任一条目的请不要加入

- 觉得特别贵
- 还没写过Vue
- 觉得是在坑钱
- 要求秒回
- 纯粹观望
- 先加入再退款

## 我想给你发个红包，怎么发

<img src="https://o3e85j0cv.qnssl.com/vux_pay.png" width="450">
