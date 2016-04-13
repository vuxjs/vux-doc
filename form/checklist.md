# checklist 多选

## API

| 参数         | 说明                  | 类型        | 默认值 |
| ----------- | ---------------------- | ---------- | ------- |
| title | 选项标题 | String | 无 |
| required| 可选，是否为必选项 | Boolean | true |
| options | 选项数组 | Array | 无 |
| value | 可选，已选择条目值 | Array | 无 |
| max | 可选，至多选择条目个数 | Number | 无 |
| min | 可选，至少选择条目个数 | Number | 无 |
| random-order | 可选，是否打乱条目排序 | Boolean | false |

> 当设置`required=false`时，`min`设置将无效，即最少选定个数为0

## 示例

### 基本使用

``` vux height=240 components=Checklist

<template>
<checklist title="请选择你的爱好" :options="hobbies" :value.sync="hobby" @change="change"></checklist>
</template>
<script>
export default {
  data () {
  	return {
  		hobbies: ['篮球', '足球', '羽毛球', '打飞机'],
  		hobby: ['打飞机']
  	}
  },
  methods: {
  	change (val) {
  		console.log('change', val)
  	}
  }
}
</script>
```

### 设定选择条目个数

``` vux height=250 components=Checklist

<template>
<checklist title="至多选择两项" :options="items" :value.sync="selectedItems" :max=2 :required=false @change="change"></checklist>
</template>
<script>
export default {
  data () {
    return {
      items: ['篮球', '足球', '羽毛球', '台球'],
      selectedItems: []
    }
  },
  methods: {
    change (val) {
      console.log("change", val)
    }
  }
}
</script>

```


### key-value类型数组展示

> 每个条目的`key`必须为字符串

``` vux height=200 components=Checklist

<template>
<checklist title="Please select" :options="objectList" :value.sync="objectListValue"></checklist>
</template>
<script>
export default {
	data () {
		return {
			objectList: [{key: '1', value: '001 value'}, {key: '2', value: '002 value'}, {key: '3', value: '003 value'}],
			objectListValue: ['1', '2']
		}
	}
}
</script>
```

### 打乱展示顺序

``` vux height=250 components=Checklist

<template>
<checklist title="随机顺序显示" :options="items" :value.sync="selectedItems" random-order></checklist>
</template>
<script>
export default {
  data () {
    return {
      items: ['篮球', '足球', '羽毛球', '台球'],
      selectedItems: []
    }
  }
}
</script>

```