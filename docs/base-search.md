### BaseSearch

通用查询组件，封装了基本查询操作。

<iframe width="100%" height="400" src="http://jsfiddle.net/jianglin/rkzpLx0s/24/embedded/result"></iframe>

```html
<template>
  <base-search :fields="fields" @onSearch="handleSomething"></base-search>
</template>

<script>
  export default {
    data() {
      return {
        fields: [{
          value: '黄金糕',
          label: '黄金糕',
        }, {
          value: '双皮奶',
          label: '双皮奶',
        }, {
          value: '蚵仔煎',
          label: '蚵仔煎',
        }, {
          value: '龙须面',
          label: '龙须面',
        }, {
          value: '北京烤鸭',
          label: '北京烤鸭',
        }],
      };
    },
    methods: {
      handleSomething(data) {
        console.log(data); // eg: [{seqNo: 1, field: 'xx', value: 'xxx', condition: '', and: ''},{...}]
      },
    },
  };
</script>
```

### Attributes

<table style="text-align:left">
  <tr>
    <th style="width: 200px">参数</th>
    <th style="width: 200px">说明</th>
    <th style="width: 200px">类型</th>
    <th style="width: 200px">可选值</th>
    <th style="width: 200px">默认值</th>
  </tr>
  <tr>
      <th>fields</th>
      <th>描述字段</th>
      <th>Array</th>
      <th>-</th>
      <th>-</th>
  </tr>

</table>

### Events

<table style="text-align:left">
  <tr>
    <th style="width: 200px">事件名称	</th>
    <th style="width: 500px">说明</th>
    <th style="width: 200px">回调参数</th>
  </tr>
  <tr>
    <th>onSearch</th>
    <th>查询回调方法</th>
    <th>已选择的查询条件</th>
  </tr>
</table>
