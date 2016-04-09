# 倒计时

## 常用场景

+ 活动报名、商品折扣时间倒计时
+ 有效支付时间倒计时

## 选项



## 示例

### 一般使用

``` vux height=60 components=Clocker
<template>
<p style="padding:15px;">
  <span>距离2017-04-01还有</span>
  <clocker time="2017-04-01"></clocker>
</p>
</template>
```

### 在Cell中使用

``` vux height=65 components=Clocker,Group,Cell
<template>
<group>
  <cell title="20170401">
    <clocker time="2017-04-01" slot="value"></clocker>
  </cell>
</group>
</template>
```
### 自定义html模板

> 分割数字只支持两位日期，如果有两位以上，可以考虑使用`on-tick`事件来处理

``` vux height=120 components=Clocker,Group,Cell
<template>
<group>
  <cell title="Date:0501">
    <clocker time="2016-05-01" slot="value">
      <span style="color:red">%D 天</span>
      <span style="color:green">%H 小时</span>
      <span style="color:blue">%M 分 %S 秒</span>
    </clocker>
  </cell>
  <cell title="分割两位数字">
    <clocker time="2018-08-08" slot="value">
      <span class="day">%_D1</span>
      <span class="day">%_D2</span>天
      <span class="day">%_H1</span>
      <span class="day">%_H2</span>时
      <span class="day">%_M1</span>
      <span class="day">%_M2</span>分
      <span class="day">%_S1</span>
      <span class="day">%_S2</span>秒
    </clocker>
  </cell>
</group>
</template>

<style>
.day {
  background-color:#000;
  color:#fff;
  text-align:center;
  display:inline-block;
  padding:0 3px;
  border-radius:3px;
}
</style>
```

