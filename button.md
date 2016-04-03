# Button 按钮


### 一般使用

{% vux components="XButton",height=170 %}
<template>
<x-button>submit</x-button>
<x-button type="primary">primary</x-button>
<x-button type="warn">Delete</x-button>
</template>
{% endvux%}


### 不可点击

{% vux components="XButton",height=170 %}
<template>
<x-button disabled>submit</x-button>
<x-button type="primary" disabled>primary</x-button>
<x-button type="warn" disabled>Delete</x-button>
</template>
{% endvux%}

### 直接用:text指定按钮文字

{% vux components="XButton",height=50 %}
<template>
<x-button type="primary" :text="btnText" :disabled="isDisabled" @click="click"></x-button>
</template>

<script>
export default {
  data: {
    btnText: 'click me',
    isDisabled: false
  },
  methods: {
    click: function () {
      const _this = this
      this.isDisabled = true
      this.btnText = 'Processing'
      setTimeout(function () {
        _this.btnText = 'Done'
      }, 2000)
    }
  }
}
</script>
{% endvux%}
