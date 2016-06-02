# PR 规范

+ 提交前确认已经`rebase`了开发分支代码
+ 只修改组件源代码，不需要进行`xbuild`操作
+ 遵从代码缩进规范，确认`npm run dev`时没有`eslint`错误
+ 如果添加了新的`feature`或者修复了某个bug, 需要在相应的demo文件增加example

## Commit Message

提交消息如果是修改了特定组件，请使用组件名+冒号+英文空格+英文提交信息的形式 
  
  粟子: `Cell: Add some prop`


## 特定组件依赖

带有子组件并且有selected状态的需要使用multi-mixin, 工具库位于`src/mixins/multi-items.js`，可以参考`button-tab`、`tabbar`等组件。
