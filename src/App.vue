<script setup>
  import {ref} from "vue";

  const num1 = ref();
  num1.value = 2

  const num2 = ref(0);
  num2.value = 3

</script>

<template>
  <div>
    <span>Num1: </span>
    <span>{{ num1 }}</span>
  </div>

  <div>
    <span>Num2: </span>
    <span>{{ num2 }}</span>
  </div>


</template>

<style scoped>

</style>
