<template>
  <h2>Números ingresados</h2>
  <p>Número 1: {{ n1 }}</p>
  <p>Número 2: {{ n2 }}</p>
  <p>Número 3: {{ n3 }}</p>
  <h2>Cantidad iguales</h2>
  <p>{{ iguales }}</p>
</template>

<script>
export default {
  name: "CantidadIguales",
  props: {
    n1: Number,
    n2: Number,
    n3: Number,
  },
  computed: {
    iguales() {
      let t = 0;
      this.n1 === this.n2 ? t++ : null;
      this.n3 === this.n2 ? t++ : null;
      this.n1 === this.n3 ? t++ : null;
      return t === 1 ? 2 : t;
    },
  },
};
</script>

<style scoped></style>
