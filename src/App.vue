<script setup>
const name = ', mi primer proyecto';
const styleColor = 'color: green';
</script>

<template>
  <!--<h1 v-bind:style="styleColor">Hola Zalma{{ name }}</h1>-->
  <h1 :style="styleColor">Hola Zalma{{ name }}</h1>
</template>

<style>
h1{
  color:red
}
</style>