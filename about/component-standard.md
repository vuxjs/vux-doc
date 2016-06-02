# 开发规范

## 0. 代码规范

### 主要原则

+ 使用最新es6语法
+ 通过项目的eslint

### 具体细则

+ 用`const`或者`let`代替`var`
+ 依赖包括工具函数分离成单独的js文件`import`

## 1. 组件

### 组件命名

+ 尽量简单、标准。如果与原生标签一样，在前面加上`x`，如`x-input`,`x-textarea`,`x-img`
+ export 出来的对象命名为`驼峰式`，如`Radio`,`XInput`,`XTextarea`
+ 假设存子组件，子组件命名在父组件后面加上`-item`, 如`flexbox`及`flexbox-item`, `tab`及`tab-item`

### 组件目录

+ 每个组件为单独的目录，位于`src/components/`下，目录名全小写，入口文件为`index.vue`
+ 若项目包含子组件，入口文件同样为`index.vue`，同时目录下包含与组件名同名的文件，如`tab.vue`、`tab-item.vue`

### 组件属性

+ 必须规定`type`或者`validator`进行类型验证
+ 不要加`coerce`

## 2. 事件

### 命名

+ 统一以on前缀，如on-change。这样规范的原因：
  + 避免与原生事件(如 `change`) 同名冲突重复收到DOM事件且参数错误
  + 容易读写，与其他类型属性区分

## 3. 模板

+ 不能为`片断`模板(不会暴露至外部使用的公用小组件除外)
+ `class`和`style`超过两个属性要写到`computed`里

## 4. 版本发布

+ 修改`package.json`的version
+ 添加`git tag`
+ `npm publish`
+ `git push origin master`
+ `git push origin tag`
+ 登录`Github`修改最新release的发布信息