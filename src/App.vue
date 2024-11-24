<script setup>
import {reactive, ref} from "vue";

// 定义对象
const userList = reactive([
  {
    "id": 1,
    "name": "小甜甜",
    "age": 18,
    "sex": "女",
  },
  {
    "id": 2,
    "name": "小甜甜",
    "age": 19,
    "sex": "男",
  },
  {
    "id": 3,
    "name": "小甜甜",
    "age": 20,
    "sex": "女",
  },
  {
    "id": 4,
    "name": "小甜甜",
    "age": 21,
    "sex": "保密",
  },
])

</script>

<template>

  <div class="container">
    <table>
      <thead>
      <tr>
        <th>学号</th>
        <th>姓名</th>
        <th>年龄</th>
        <th>性别</th>
      </tr>
      </thead>
      <tbody>
      <tr v-for="(item, index) in userList" :data-index="index">
        <td>{{ item.id }}</td>
        <td>{{ item.name }}</td>
        <td>{{ item.age }}</td>
        <td v-if="item.sex === '男'" style="background-color: blue;color: white">{{ item.sex }}</td>
        <td v-else-if="item.sex === '女'" style="background-color: red;color: white">{{ item.sex }}</td>
        <td v-else style="background-color: orange;color: white">{{ item.sex }}</td>
      </tr>
      </tbody>
    </table>
  </div>

</template>

<style scoped>
.container {
  width: 800px;
  margin: 0 auto;
}

table {
  width: 800px;
  border: 1px solid black;
  border-spacing: 0;
  text-align: center;
}

th, td {
  border: 1px solid black;
  height: 30px;
}
</style>
