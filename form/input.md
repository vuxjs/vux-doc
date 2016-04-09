# x-input 单行文本输入

> 命名为`x-input`避免与原生`input`标签渲染冲突

## 属性
+ keyboard 只支持 `number`,用于激活数字键盘

## 验证

+ min-length 最小字符长度
+ max-length 最大字符长度
+ pattern 正则匹配, 同原生input pattern
+ is-type 内置类型验证


### is-type 类型
+ china-name 中文姓名
+ email 邮箱
+ url 链接
+ china-mobile 手机号码
+ ip ip 地址
+ number 数字
``` html
<x-input :min=1 :max=10></x-input>
```