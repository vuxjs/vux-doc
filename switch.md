# Switch

> 作为行内表单组件，`Switch`必须和`Group`一起使用。

## 直接值

{% vux height=160 %}
<components>
Switch,Group
</components>
<template>
<group>
  <switch title="Switch" :value=true></switch>
  <switch title="Switch" :value=false></switch>
</group>
</template>
{% endvux %}

## 双向绑定

{% vux height=80 %}
<components>
Switch,Group
</components>
<template>
<group>
  <switch :title="'双向绑定:值为' + value1" :value.sync="value1"></switch>
</group>
</template>

<script>
export default {
  data: {
    value1: true
  }
}
</script>
{% endvux %}


### disabled 设置不可更改

{% vux height=140 %}
<components>
Switch,Group
</components>
<template>
<group>
  <switch title="不可更改" :value=true disabled></switch>
  <switch title="不可更改" :value=false disabled></switch>
</group>
</template>
{% endvux %}

### title支持html

{% vux height=80 %}
<components>
Switch,Group
</components>
<template>
<group>
  <switch title="<span style='color:red'>红色文字</span>" :value=true></switch>
</group>
</template>
{% endvux %}

### on-change 事件

{% vux height=80 %}
<components>
Switch,Group
</components>
<template>
<group>
  <switch title="监听事件" :value=true @on-change="change"></switch>
</group>
</template>
<script>
export default {
  methods: {
    change: function (val) {
      console.log('change', val)
    }
  }
}
</script>
{% endvux %}


