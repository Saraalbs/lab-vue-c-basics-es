<script setup>
import { ref } from "vue";

const suma = ref(2 + 2);

//Imprimir string con variables reactivas (Iteración 1)
const nombre = ref("Sara");
const apellido = ref("Alborés");

//Función que devuelve la cadena de variables
function saludo() {
  return `Hola, mi nombre es ${nombre.value} ${apellido.value}`;
}

//Operación suma (Iteración 1)
setInterval(() => {
  suma.value = suma.value + 1;
}, 1000);
</script>

<template>
  <h2>Counter: {{ suma }}</h2>
  <div>
    {{ saludo() }}
  </div>
</template>

<style scoped></style>
