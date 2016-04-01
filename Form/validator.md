# Validator


> `不能`依赖前端验证，后端必须同样做验证。

唯一需要设置的是`name`属性，用于保存验证信息
如果想实现更可读的数据，即`serialize`后的数据，需要为每个表单设置`name`属性，否则返回的`data` key 都为每个表单的`uuid`。

验证信息属性:

+ valid 是否验证通过
+ invalid 是否验证不通过
+ data 表单数据，不包含`disabled`的表单值
+ allData 所有表单数据，包含`disabled`的表单值

{% vux with=100% %}
<validator name="demo">
  <input type="submit" value="send" v-if="$demo.valid">
</validator>
{% endvux %}