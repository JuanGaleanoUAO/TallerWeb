<template>
  <input
    id="value1"
    type="number"
    placeholder="Ingresa valor 1"
    v-model="value1"
  />
  <button v-on:click="Ordenar(value1)">Agregar a la lista</button>
  <br />
  <span>{{ lista }}</span>
</template>

<script>
import { watch } from "@vue/runtime-core";
export default {
  data() {
    return {
      lista: [],
      value1: "",
      a: "",
    };
  },

  methods: {
    Ordenar(value1) {
      this.lista.push(value1);
      this.lista.sort(function (a, b) {
        return a - b;
      });
      return "La lista es" + this.lista;
    },
  },

  watch: {},
};
</script>

<style scoped></style>
