<template>
  <h2>Digite la posición por la cual dividir el arreglo</h2>
  <input type="number" v-model="posicion" />
  <h2>Arreglo dividido</h2>
  <p v-if="posicion < 0">[]</p>
  <p v-if="posicion < 0">[]</p>
  <p v-if="posicion >= 0">{{ arreglo.slice(0, posicion) }}</p>
  <p v-if="posicion >= 0">{{ arreglo.slice(posicion) }}</p>
</template>

<script>
export default {
  name: "DividirArreglo",
  props: {
    arreglo: Array,
  },
  data() {
    return {
      posicion: 0,
    };
  },
};
</script>

<style scoped></style>
