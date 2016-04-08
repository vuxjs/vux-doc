# playground

## 页面接口

### https://vux.li/api/v1/demo.html

> 简易接口，用于把代码拼凑成完整的vue页面，文档中的例子都是使用该接口以iframe嵌入。

> 注意`GET`方式url长度有限制，所以这种方式用于相对简单的例子。

### url参数

+ `components` 使用的组件，英文逗号分隔，如 `Group,Radio`
+ `javascript` js代码，以`export default {`开头， `}`结束
+ `template` 模板，普通`html`代码
+ `style` 样式,只支持一般css，不支持指定`lang`及`scoped`


## 在文档中的例子：

> 注意的是 Gitbook会渲染双花括号,因此所有的花括号用`<<>>`代替，render时会自动替代成正确的。

``` html
<span> {{arg}} </span>
=>
<span> <<arg>> </span>
```

因为Gitbook会错误渲染源代码，因此请看这里的粟子: [Circle.md](https://raw.githubusercontent.com/vuxjs/vux-doc/master/chart/circle.md)