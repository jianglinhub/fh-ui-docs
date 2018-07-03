### BaseSearch

通用查询组件，封装了基本查询操作。

#### 代码示例
```html
<template>
  <div class="demo">
    <base-search :fields="fields" @onSearch="handleSomething"></base-search>
  </div>
</template>

<script>
  // 引入通用查询组件
  import SearchSub from './search-sub'

  export default {
    name: 'demo',
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
      }
    },
    components: {
      // 添加引入的组件
      SearchSub
    },
    methods: {
      handleSomething(data) {
        console.log(data) // eg: [{seqNo: 1, field: 'xx', value: 'xxx', condition: '', and: ''},{...}]
      }
    }
  }
</script>
```

### Attributes

<table>
  <tr>
    <th style="width: 200px">参数</th>
    <th style="width: 200px">说明</th>
    <th style="width: 200px">类型</th>
    <th style="width: 200px">可选值</th>
    <th style="width: 200px">默认值</th>
  </tr>
  <tr>
      <th>fields</th>
      <th>描述字段儿</th>
      <th>Array</th>
      <th>-</th>
      <th>[]</th>
  </tr>
  
</table>

### Events

<table>
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