<template>
  <h2>Numero a agregar</h2>
  <input type="number" v-model="numero" />
  <input type="button" value="Agregar" @:click="agregarALista" />
  <h3>Lista</h3>
  <p>{{ lista }}</p>
</template>

<script>
export default {
  name: "AgregarOrdenar",
  data() {
    return {
      numero: 0,
      lista: [],
    };
  },
  methods: {
    agregarALista() {
      this.lista.push(this.numero);
      this.lista.sort();
    },
  },
};
</script>

<style scoped></style>
