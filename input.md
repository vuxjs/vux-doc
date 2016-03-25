# x-input 单行文本输入

> 命名为`x-input`避免与原生`input`标签渲染冲突

## 属性


## 验证

+ minLength 最小字符长度
+ maxLength 最大字符长度
+ pattern 正则匹配, 同原生input pattern

``` html
<x-input :min=1 :max=10></x-input>
```