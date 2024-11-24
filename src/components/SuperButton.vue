<script setup>
defineProps(["color"]);
</script>

<template>
<button :class="['btn', 'btn-' + color]" >
  <slot></slot>
</button>
</template>

<style scoped>
.btn{
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.5;
  text-align: center;
  text-decoration: none;
  padding: .375rem .75rem;
  margin: .25rem .125rem;
  border-radius: .25rem;
  border: 1px solid transparent;
  transition: color .15s ease-in-out,background-color .15s ease-in-out,border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  cursor: pointer;
}
.btn-primary{
  color: #fff;
  background-color: #0d6efd;
  border-color: #0d6efd;
  font-weight: 400;
}
.btn-secondary{
  color: #fff;
  background-color: #6c757d;
  border-color: #6c757d;
}
.btn-success{
  color: #fff;
  background-color: #198754;
  border-color: #198754;
}
.btn-danger{
  color: #fff;
  background-color: #dc3545;
  border-color: #dc3545;
}
.btn-warning{
  color: #000;
  background-color: #ffc107;
  border-color: #ffc107;
}
.btn-info{
  color: #000;
  background-color: #0dcaf0;
  border-color: #0dcaf0;
}
.btn-dark{
  color: #fff;
  background-color: #212529;
  border-color: #212529;
}
</style>