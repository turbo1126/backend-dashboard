<template>
  <el-table
    :data="tableData.filter(data => !search || data.name.toLowerCase().includes(search.toLowerCase()))"
    style="width: 100%">
    <el-table-column
       prop="date"
      label="日期"
      sortable
      width="180">
    </el-table-column>
    <el-table-column
      label="姓名"
      prop="name"
      width="180">
    </el-table-column>
    <el-table-column
      label="班级"
      prop="class"
      width="180">
    </el-table-column>

    <el-table-column
      align="right">
      <template slot="header" >
        <el-input
          v-model="search"
          size="mini"
          placeholder="输入关键字搜索"/>
      </template>
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
  export default {
    data() {
      return {
        tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          class:'艺设211'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          class:'艺设211'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          class:'艺设211'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          class:'艺设211'
        }],
        search: ''
      }
    },
    methods: {
      handleEdit(index, row) {
        console.log(index, row);
      },
      handleDelete(index, row) {
        console.log(index, row);
      }
    },
  }
</script>