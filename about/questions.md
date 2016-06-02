# 常见问题

## 为什么文档这么久才写完

主要是懒。

## 其他格式的文档有么?

+ [PDF](https://www.gitbook.com/download/pdf/book/vuxjs/vux)
+ [ePub](https://www.gitbook.com/download/epub/book/vuxjs/vux)
+ [Mobi](https://www.gitbook.com/download/mobi/book/vuxjs/vux)

## 不懂Vue， 怎么用

你给我滚出去

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

没有，不喜欢用QQ群，并且QQ群交流容易变成吹水消息混乱不好跟踪管理，但是可以提`issue`或者加入 [vux@bearychat](https://vux.bearychat.com/)，问题都会得到较快回复。

## 如何加入Vux开发

PR即可。也可以邮件到`i@mao.li`申请加入 [vux@teambition](https://www.teambition.com/project/56f37e966d3fb3142656b764/tasks/scrum/56f37e969aff544c264e23ec)

## 我想给你发个红包，怎么发

<img src="https://o3e85j0cv.qnssl.com/vux_pay.png" width="450">