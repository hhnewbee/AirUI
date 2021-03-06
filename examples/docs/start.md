
# 快速上手

----

## 使用前准备

> 在使用之前，推荐学习 `Vue` 和 `ES6` ，并正确配置 `Node.js` v7.x 或以上版本

### 全局使用

1. 在项目的入口文件中引入所有组件或所需组件

```js
import AirUI from 'airui-vue' // 引入组件库
import 'airui-vue/theme/css/index.css' // 引入样式库

Vue.use(AirUI)
```
2. 在模板中，用 `<air-index-select></air-index-select>` 自定义标签的方式使用组件

```html
<template>
  <air-index-select />
</template>
```


### 按需使用

1. 局部注册所需的组件，适用于与其他框架组合使用的场景

**注意:**css文件使用蛇形文件名

```js

import AirIndexSelect from 'airui-vue/components/AirIndexSelect'
import 'airui-vue/theme/css/air-index-select.css'

Vue.component('AirIndexSelect', AirIndexSelect)
```
2. 修改webpack配置文件
```json
module: {
  rules: [
  ...
    {
      test: /airui-vue.*?js$/,
      loader: 'babel-loader'
    }
   ...
  ]
}
```

3. 在模板中，用 `<air-index-select></air-index-select>` 自定义标签的方式使用组件

```html
<template>
  <air-index-select />
</template>
```

## 自定义主题

开发中...
