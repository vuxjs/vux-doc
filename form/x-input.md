# x-input 单行文本输入

> 命名为`x-input`避免与原生`input`标签渲染冲突


> 注意不要混淆：`x-input`不是原生`input`,不能使用`v-model`,数据绑定语法为`:value.sync`

## 属性
+ title 输入框标题
+ inline-desc 标题下方描述
+ keyboard 只支持 `number`,用于激活数字键盘
+ placeholder 输入提示
+ show-clear 是否显示清除按钮
+ type 输入类型，与原生`input`属性相同,默认为text

## 验证

+ min 最小字符长度
+ max 最大字符长度
+ pattern 正则匹配, 同原生input pattern
+ is-type 内置类型验证
+ required 非空
+ equal-with 等值判断


### is-type 类型
+ china-name 中文姓名
+ email 邮箱
+ url 链接
+ china-mobile 手机号码
+ ip ip 地址
+ number 数字
``` html
<!-- 必须输入6-10位的电子邮件地址 -->
<x-input :min=6 :max=10 is-type=email></x-input>
<!-- 手机号码验证 -->
<x-input 
    title="手机号"
    is-type="china-mobile" 
    :show-clear=true 
    placeholder="请输入手机号"></x-input>
<!-- 必须输入123456 -->
<x-input
    title="等值判断"
    type="text"
    equal-with="123456"></x-input>
```

## slot

> 悬浮在输入框最右边的元素，必须设置为slot="left"

``` html
<x-input title="发送验证码" class="weui_vcode">
    <img slot="left" src="http://weui.github.io/weui/images/vcode.jpg">
</x-input>
```
