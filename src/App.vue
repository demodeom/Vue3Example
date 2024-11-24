<script setup>
  import {reactive} from "vue";

  // 定义对象
  const userInfo = reactive({
    "name": "小甜甜",
    "age": 18,
    "sex": "女",
  })

  const increaseAge = (num=1) => {
    userInfo.age += num;
  }

  const decreaseAge = (num=1) => {
    userInfo.age -= num;
  }

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

  <div>
    <button v-on:click="increaseAge()">加 1 岁</button>
    <button v-on:click="decreaseAge()">减 1 岁</button>
  </div>


  <div>
    <button v-on:click="increaseAge(5)">加 5 岁</button>
    <button v-on:click="decreaseAge(5)">减 5 岁</button>
  </div>

  <div>

  </div>

</template>

<style scoped>
div{
  padding: 10px;
}

button{
  margin-right: 20px;
}
</style>
