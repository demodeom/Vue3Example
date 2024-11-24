<script setup>
  import {reactive} from "vue";

  // 定义对象
  const userInfo = reactive({
    "name": "小甜甜",
    "age": 18,
    "sex": "女",
  })

  // 修改对象值
  userInfo.age = 19

</script>

<template>

  <div>
    <span>姓名: </span>
    <span>{{ userInfo.name }}</span>
  </div>

  <div>
    <span>年龄: </span>
    <span>{{ userInfo.age }}</span>
  </div>

  <div>
    <span>性别: </span>
    <span>{{ userInfo.sex }}</span>
  </div>

</template>

<style scoped>

</style>
