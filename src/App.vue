<script setup>
const name = ', mi primer proyecto';
const styleColor = 'color: green';
const arrayColores = [ "blue", "red","pink", "purple" ]
const activo = true;
</script>

<template>
  <!--<h1 v-bind:style="styleColor">Hola Zalma{{ name }}</h1>-->
  <h1 :style="styleColor">Hola Zalma{{ name }}</h1>
  <h1 :style="styleColor">Hola Zalma{{ name.toUpperCase ()}}</h1>
  <h2 :style="`color: ${arrayColores[3]}`">Prueba de color</h2> <!--Interpolacion-->
  <h2>{{ activo ? "Estoy activo" : "Estoy inactivo" }}</h2>
</template>

<style>
h1{
  color:red
}
</style>