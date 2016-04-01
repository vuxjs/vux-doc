# Validator

1. 设置`name`属性，用于保存验证信息
2. 
``` html
<validator name="demo">
  <input type="submit" value="send" v-if="$demo.valid">
</validator>
```