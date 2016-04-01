# Validator

1. 设置`name`属性，用于保存验证信息

{% vux %}
<validator name="demo">
  <input type="submit" value="send" v-if="$demo.valid">
</validator>
{% endvux %}