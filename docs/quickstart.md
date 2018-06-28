### 快速开始

#### 使用之前

有必要了解Vue基础知识哦，假设你已经用过Vue，并掌握如下内容。
* Vue组件
* 单文件组件
* `props`
* `slot`
* `events` `$emit` `@click`等

fh-ui是基于`element-ui`进行的开发，所以你需要提前安装`element-ui`，安装方法请参照`element-ui`[官方文档](http://element.eleme.io/#/zh-CN/component/installation)。

#### 引入 fh-ui 
一般在 webpack 入口页面 main.js 中如下配置：
```js
import Vue from 'vue'
import Element from 'element-ui';
import FHUi from 'fh-ui';
import 'element-ui/lib/theme-chalk/index.css';
import 'fh-ui/lib/static/style.min.css';
import App from './App';
import router from './router';

Vue.use(Element);
Vue.use(FHUi);

Vue.config.productionTip = false;

/* eslint-disable no-new */
new Vue({
  el: '#app',
  router,
  components: { App },
  template: '<App/>',
});
```

#### 特别提醒
你需要导入fh-ui的样式，即在 `main.js` 或根组件执行 `import fh-ui/lib/static/style.min.css`，该文件包含了对`element-ui`的自定义样式优化，所以请保证它是在引入`element-ui`的样式文件之后引入的。