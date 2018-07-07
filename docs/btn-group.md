### BtnGroup

功能按钮组件，封装了常用的按钮操作，目前分为两类，左按钮组和右按钮组。

#### 左按钮组 btn-left-group

<iframe width="100%" height="400" src="http://jsfiddle.net/jianglin/t36j8ke0/3/embedded/result"></iframe>

```html
<template>
  <btn-left-group
    :btns="leftBtns"
    :options="leftOptions"
    @handleDelClose="handleDelClose"
    @handleDelConfirm="handleDelConfirm">
  </btn-left-group>
</template>

<script>
  export default {
    data() {
      return {
        leftBtns: ['add', 'del', 'update'],
        leftOptions: {
          addOptions: {
            router: 'testadd',
            params: {
              name: 'username',
              id: '1',
            },
          },
          delOptions: {
            id: '2',
          },
          updateOptions: {
            router: 'testupdate',
            query: {
              id: '1',
            },
          },
        },
      };
    },
    methods: {
      handleDelClose() {
        console.log('do something after handleDelClose!');
      },
      handleDelConfirm() {
        console.log('do something after handleDelConfirm!');
      },
    },
  }
</script>
```

#### 右按钮组 btn-right-group

<iframe width="100%" height="200" src="http://jsfiddle.net/jianglin/t36j8ke0/5/embedded/result"></iframe>

```html
<template>
  <btn-right-group
    :btns="rightBtns"
    :options="rightOptions">
  </btn-right-group>
</template>

<script>
  export default {
    data() {
      return {
        rightBtns: ['refresh', 'close'],
        rightOptions: {},
      };
    },
  }
</script>
```

#### 左按钮组 Attributes

<table style="text-align:left">
  <tr>
    <th style="width: 100px">参数</th>
    <th style="width: 300px">说明</th>
    <th style="width: 100px">类型</th>
    <th style="width: 400px">可选值</th>
    <th style="width: 100px">默认值</th>
  </tr>
  <tr>
      <th>btns</th>
      <th>需要显示的按钮集合</th>
      <th>Array</th>
      <th>add（添加）, del（删除）, update（修改）, check（批改）, startUse（启用）</th>
      <th>-</th>
  </tr>
  <tr>
      <th>options</th>
      <th>按钮参数</th>
      <th>Object</th>
      <th>详见left-group-options按钮参数列表</th>
      <th>-</th>
  </tr>
</table>

#### left-group-options 按钮参数列表
<table style="text-align:left">
  <tr>
    <th style="width: 100px">参数</th>
    <th style="width: 300px">说明</th>
    <th style="width: 100px">类型</th>
    <th style="width: 400px">可选值</th>
    <th style="width: 100px">默认值</th>
  </tr>
  <tr>
      <th>addOptions</th>
      <th>添加按钮所需参数</th>
      <th>Object</th>
      <th>router（页面地址，必传）, params, query</th>
      <th>-</th>
  </tr>
  <tr>
      <th>delOptions</th>
      <th>删除按钮所需参数</th>
      <th>Object</th>
      <th>id（删除项的id，必传）</th>
      <th>{id: '0'}</th>
  </tr>
  <tr>
      <th>updateOptions</th>
      <th>修改按钮所需参数</th>
      <th>Object</th>
      <th>router（页面地址，必传）, params, query</th>
      <th>-</th>
  </tr>
  <tr>
      <th>checkOptions</th>
      <th>批改按钮所需参数</th>
      <th>Object</th>
      <th>router（页面地址，必传）, params, query</th>
      <th>-</th>
  </tr>
  <tr>
      <th>startUseOptions</th>
      <th>启用按钮所需参数</th>
      <th>Object</th>
      <th>id（启用项的id，必传）</th>
      <th>{ id: '0' }</th>
  </tr>
</table>

#### 左按钮组 Events

<table style="text-align:left">
  <tr>
    <th style="width: 200px">事件名称	</th>
    <th style="width: 500px">说明</th>
    <th style="width: 200px">回调参数</th>
  </tr>
  <tr>
    <th>handleDelClose</th>
    <th>取消删除回调方法</th>
    <th>-</th>
  </tr>
  <tr>
    <th>handleDelConfirm</th>
    <th>确定删除回调方法</th>
    <th>-</th>
  </tr>
</table>

#### 右按钮组 Attributes

<table style="text-align:left">
  <tr>
    <th style="width: 100px">参数</th>
    <th style="width: 300px">说明</th>
    <th style="width: 100px">类型</th>
    <th style="width: 400px">可选值</th>
    <th style="width: 100px">默认值</th>
  </tr>
  <tr>
      <th>btns</th>
      <th>需要显示的按钮集合</th>
      <th>Array</th>
      <th>refresh（刷新）, close（关闭）, print（打印）</th>
      <th>-</th>
  </tr>
  <tr>
      <th>options</th>
      <th>按钮参数</th>
      <th>Object</th>
      <th>详见right-group-options按钮参数列表</th>
      <th>-</th>
  </tr>
</table>

#### left-group-options 按钮参数列表

### 待补充...
