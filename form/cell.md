# cell

{% vux components='Cell,Group' %}
<template>
<group>
  <cell title="My Account" value="Protected" @click="click"></cell>
</group>
</template>
<script>
export default {
  methods: {
    click: function () {
      alert('click')
    }
  }
}
</script>
{% endvux %}