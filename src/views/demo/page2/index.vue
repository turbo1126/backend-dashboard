<template>
  <el-table
    :data="tableData"
    style="width: 100%">
    <el-table-column
      prop="id"
      label="编号"
      width="180">
    </el-table-column>
    <el-table-column
      prop="name"
      label="名称"
      width="180">
    </el-table-column>
    <el-table-column
      prop="date"
      label="创建时间">
    </el-table-column>
    <el-table-column
      prop="select"
      label="选择人数">
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  data () {
    return {
      tableData: [{
        id:'01',
        name: '虚拟仿真实验一',
        date: '2021-05-04',
        select: '63'
      }, {
        id:'02',
        name: '虚拟仿真实验二',
        date: '2021-05-04',
        select: '63'
      }, {
       id:'03',
        name: '虚拟仿真实验三',
        date: '2021-05-04',
        select: '63'
      }, {
        id:'04',
        name: '虚拟仿真实验四',
        date: '2021-05-04',
        select: '63'
      }]
    }
  }
}
</script>
