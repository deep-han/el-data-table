axiosConfig 示例代码，打开控制台，可以看到请求中带上了自定义的头

```vue
<template>
  <el-data-table v-bind="$data" />
</template>
<script>
export default {
  data() {
    return {
      axiosConfig: {
        headers: {
          'Authorization': 'Bearer token',
          'X-TOKEN': 'X-TOKEN'
        }
      },
      url: 'https://mockapi.eolinker.com/IeZWjzy87c204a1f7030b2a17b00f3776ce0a07a5030a1b/el-data-table?q=basic',
      columns: [
        {prop: 'date', label: '日期'},
        {prop: 'name', label: '姓名'},
        {prop: 'address', label: '地址'},
      ],
      form: [
        {
          type: 'input',
          id: 'name',
          label: '姓名',
          rules: [
            {
              required: true,
              message: '请输入姓名',
              trigger: 'blur',
              transform: v => v && v.trim()
            }
          ],
          el: {placeholder: '请输入姓名'}
        },
      ],
      searchForm: [
        {
          el: {placeholder: '请输入'},
          label: '姓名',
          id: 'name',
          type: 'input'
        }
      ],
      hasView: true
    }
  }
}
</script>
```
