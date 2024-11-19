<script setup>
const name = ', mi primer proyecto';
const styleColor = 'color: green';
const arrayColores = [ "blue", "red","pink", "purple" ]
const activo = false;

// const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];
const arrayFrutas = [
    {
        name: "Manzana",
        price: "$1.00",
        description: "Una manzana",
        stock: 0,
        id:1,
    },
    {
        name: "Pera",
        price: "$2.00",
        description: "Una pera",
        stock: 10,
        id:2,
    },
    {
        name: "Naranja",
        price: "$3.00",
        description: "Una naranja",
        stock: 20,
        id:3,
    },
];

// const objetoManzana ={
//   name: "Manzana",
//   price: "$1.00",
//   description: "Una manzana",
//   stock: 0,
//   id:1,
// }
</script>

<template>
  <!-- v-bind ó : -->
  <!--<h1 v-bind:style="styleColor">Hola Zalma{{ name }}</h1>-->
  <h1 :style="styleColor">Hola Zalma{{ name }}</h1>

  <!-- Expresiones JS -->
  <!-- <h1 :style="styleColor">Hola Zalma{{ name.toUpperCase ()}}</h1>
  <h2 :style="`color: ${arrayColores[3]}`">Prueba de color</h2> Interpolacion -->
  <!-- <h2>{{ activo ? "Estoy activo" : "Estoy inactivo" }}</h2> -->

<!-- Directivas -->
  <!-- v-if -->
   <!-- <h2 v-if="activo">Estoy activo</h2>
   <h2 v-if="!activo">Estoy inactivo</h2> -->
  <!-- v-if/else -->
   <!-- <h2 v-if="activo">Estoy activo</h2>
   <h2 v-else>Estoy inactivo</h2> -->

  <!-- v-else-if -->
   <!-- <h2 v-if="activo === true">Estoy activo</h2>
   <h2 v-else-if="activo === false">Estoy inactivo</h2>
   <p v-else>Estoy indeciso</p> -->

   <!-- v-show (Pone la propiedad display:none;)-->
    <!-- <p v-show="activo">Estoy activo v-show</p> -->


  <!-- v-for -->
   <!-- <ul>
    <li v-for="fruta in arrayFrutas">{{fruta}}</li>
    <li v-for="(fruta, index) in arrayFrutas">{{index}} .- {{fruta}}</li>
    <li v-for="(fruta, index) in arrayFrutas" :key="index">{{index}} .- {{fruta}}</li>
   </ul> -->

   <!-- v-for (array de objetos)(Key es el elemento unico que no se debe de repetir) -->
    <!-- <ul>
      <li v-for="fruta2 in arrayFrutas" :key="fruta2.id">
        {{ fruta2.name }} - {{ fruta2.price }} - {{ fruta2.description }}
      </li>
    </ul> -->

    <!-- v-for (objetos) -->
     <!-- <ul>
      <li v-for="(manzana,propiedad, index) in objetoManzana" :key="index">
        {{index}}.- {{propiedad}}: {{ manzana }}
      </li>
     </ul> -->


    <!-- v-for + v-if + template -->
     <ul>
      <template v-for="item in arrayFrutas" :key="item.name">
        <li v-if="item.stock > 10"> {{ item.name }} - {{ item.price }}</li>
      </template>
     </ul>

</template>

<style>
h1{
  color:red
}
</style>