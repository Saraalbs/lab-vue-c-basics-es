<script setup>
import { ref } from "vue";

//Variable booleana (Iteración 3)
const mayorEdad = ref(true);

function mayor() {
  mayorEdad.value = true;
}

//Lista de elementos (Iteración 4)
const publicaciones = [
  {
    title: "Lab1",
    description: "HTML",
    content: "Fundamentos de HTML",
  },
  {
    title: "Lab2",
    description: "CSS",
    content: "Fundamentos de CSS",
  },
  {
    title: "Lab3",
    description: "JavaScript",
    content: "Fundamentos de JS",
  },
];
</script>

<template>
  <div>
    <p v-if="mayorEdad">Bienvenido!</p>
    <p v-else>Acceso denegado</p>
  </div>
  <ul>
    <li v-for="(publicacion, index) in publicaciones" :key="index">
      <h3>{{ publicacion.title }}</h3>
      <h4>{{ publicacion.description }}</h4>
      <h5>{{ publicacion.content }}</h5>
    </li>
  </ul>
</template>

<style scoped></style>
