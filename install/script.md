# 使用script引入

不推荐script的方式引入，在组件多的时候会存在比较多冗余的代码导致体积比较大。

但是非新项目确实存在非.vue组件的调用形式。vux提供了所有组件的压缩包以及各个组件分别打包的文件。

``` html
<!--include Vux style-->
<link rel="stylesheet" href="vux/vux.css">
<!--include Vue yourself-->
<script src="vue.js"></script>

<div id="demo">
  <group>
    <cell title="vue" value="cool"></cell>
  </group>
</div>

<!--include the components you need-->
<script src="vux/components/group/index.js"></script>
<script src="vux/components/cell/index.js"></script>

<script>
// register components
Vue.component('group', vuxGroup)
Vue.component('cell', vuxCell)

new Vue({
  el: '#demo'
})
</script>
```