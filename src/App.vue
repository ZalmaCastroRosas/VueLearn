<script setup>
const name = ', mi primer proyecto';
const styleColor = 'color: green';
const arrayColores = [ "blue", "red","pink", "purple" ]
const activo = false;
</script>

<template>
  <!-- v-bind ó : -->
  <!--<h1 v-bind:style="styleColor">Hola Zalma{{ name }}</h1>-->
  <h1 :style="styleColor">Hola Zalma{{ name }}</h1>

  <!-- Expresiones JS -->
  <h1 :style="styleColor">Hola Zalma{{ name.toUpperCase ()}}</h1>
  <h2 :style="`color: ${arrayColores[3]}`">Prueba de color</h2> <!--Interpolacion-->
  <!-- <h2>{{ activo ? "Estoy activo" : "Estoy inactivo" }}</h2> -->

<!-- Directivas -->
  <!-- v-if -->
   <h2 v-if="activo">Estoy activo</h2>
   <h2 v-if="!activo">Estoy inactivo</h2>
  <!-- v-if/else -->
   <h2 v-if="activo">Estoy activo</h2>
   <h2 v-else>Estoy inactivo</h2>

  <!-- v-else-if -->
   <h2 v-if="activo === true">Estoy activo</h2>
   <h2 v-else-if="activo === false">Estoy inactivo</h2>
   <p v-else>Estoy indeciso</p>

   <!-- v-show (Pone la propiedad display:none;)-->
    <p v-show="activo">Estoy activo v-show</p>
</template>

<style>
h1{
  color:red
}
</style>