<template>
  <div>
    <h1>ejercicio 6</h1>
    <input @keypress.enter="odd()" type="number" v-model="num" /><br />
    <p>Impares: {{ this.impares }}</p>
  </div>
</template>

<script>
export default {
  name: "ejercicio6",
  data() {
    return {
      impares: [],
      x: 0,
      num: "",
    };
  },
  methods: {
    odd() {
      while (this.x < this.num) {
        if (this.x % 2 != 0) {
          this.impares.push(this.x);
        }
        this.x += 1;
      }
    },
  },
};
</script>

<style scoped></style>
