# Validator


> `不能`依赖前端验证，后端必须同样做验证。

唯一需要设置的是`name`属性，用于保存验证信息

验证信息属性:

+ valid 是否验证通过
+ invalid 是否验证不通过
+ data 表单数据，不包含`disabled`的表单值
+ allData

{% vux %}
<validator name="demo">
  <input type="submit" value="send" v-if="$demo.valid">
</validator>
{% endvux %}