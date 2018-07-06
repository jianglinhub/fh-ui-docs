### 安装

#### NPM 安装
推荐使用 NPM 来安装（不会NPM？em......），享受生态圈和工具带来的便利，更好地和 webpack 配合使用。

```shell
$ npm install fh-ui --save
```

### CDN

```html
<!-- 引入element样式库 -->
<link rel="stylesheet" href="https://unpkg.com/element-ui/lib/theme-chalk/index.css">
<!-- 引入fh-ui样式库 -->
<link rel="stylesheet" href="http://on7oa5kzv.bkt.clouddn.com/style.min.css">
<!-- 引入vue组件库 -->
<script src="https://unpkg.com/vue/dist/vue.js"></script>
<!-- 引入element组件库 -->
<script src="https://unpkg.com/element-ui/lib/index.js"></script>
<!-- 引入fh-ui组件库 -->
<script src="http://on7oa5kzv.bkt.clouddn.com/FHUi.min.js"></script>
```

### HelloWorld
通过 CDN 的方式我们可以很容易地使用 fh-ui 写出一个 Hello world 页面。

<iframe width="100%" height="550" src="http://jsfiddle.net/jianglin/rkzpLx0s/11/embedded/html,result"></iframe>

如果您使用了 NPM 安装，并使用 webpack 作为构建工具，请继续阅读[快速上手](quickstart.md)章节。
