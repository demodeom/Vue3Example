<script setup>
import {reactive, ref} from "vue";

  // 定义对象
  const userInfo = reactive({
    "name": "小甜甜",
    "age": 18,
    "sex": "女",
  })

  const increaseAge = () => {
    userInfo.age += Number(changeNum.value);
  }

  const decreaseAge = () => {
    userInfo.age -= Number(changeNum.value);
  }

  const changeNum = ref()
  changeNum.value = 1

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
    <input type="text" v-model="changeNum" />
  </div>


  <div>
    <button v-on:click="increaseAge">增</button>
    <button v-on:click="decreaseAge">减</button>
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
