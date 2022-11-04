<template>
  <table border="1" cellpadding="0" width="100%">
    <tr>
      <th v-for="(item,index) in headData" :key="index">
        {{item.label}}
      </th>
    </tr>
    <tr v-for="(item,index) in tableData" :key="index" >
       <td v-for="(item1,index1) in headData" :key="index1" style="text-align:center">{{item[item1.key]}}</td>    
    </tr>
  </table>


</template>

<script lang='ts' setup>
import { reactive,ref,onMounted} from 'vue'
const count = ref(0)
const headData=[
  {
    label:"日期",
    key:"date"
},
{
    label:"姓名",
    key:"name"
},
{
    label:"地址",
    key:"address"
}
]
const  tableData= [{
            date: '2016-05-02',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1518 弄'
          }, {
            date: '2016-05-04',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1517 弄'
          }, {
            date: '2016-05-01',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1519 弄'
          }, {
            date: '2016-05-03',
            name: '王小虎',
            address: '上海市普陀区金沙江路 1516 弄'
          }]
</script>
<style scoped>
</style>