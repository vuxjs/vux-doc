# x-textarea
多行文本输入框

## API
| 参数         | 说明          | 类型       | 默认值     | 双向绑定    |
| -------     | ------------- | ------     | --------- | ---------- |
| required    | 是否必填       | Boolean    | true      | false      |
| showCounter | 是否显示字数统计（需要设置max） | Boolean  | true     | false           |
| max         | 最大字符数，超出字符数 | Number |        | false      |
| value       | 绑定的值字段   | String     | ''        | true       |
| placeholder | placeholder   | String     | ''        | false      |

## Demo
* 普通的多行输入框
``` vux height=143 components=Group,XTextarea
<template>
  <group title="textarea">
    <x-textarea :max="200" placeholder="请输入详细描述"></x-textarea>
  </group>
</template>
```


* 不显示字数统计
``` vux height=143 components=Group,XTextarea
<template>
  <group title="不显示字符统计">
    <x-textarea :max="200" placeholder="请输入详细描述" :show-counter="false"></x-textarea>
  </group>
</template>
```
