<template>
  <h1>indicador respitente</h1>
  <input type="text" v-model="numero1" />
  <input type="text" v-model="numero2" />
  <input type="text" v-model="numero3" />
  <button @click="newmessage">ordenar</button>
  <p>{{ answer }}</p>
</template>

<script>
export default {
  data() {
    return {
      numero1: "",
      numero2: "",
      numero3: "",
      answer: "",
    };
  },
  methods: {
    newmessage() {
      if (this.numero1 == this.numero2) {
        this.answer = "1 es igual a 2";
      } else if (this.numero2 == this.numero3) {
        this.answer = "2 es igual a 3";
      } else if (this.numero1 == this.numero3) {
        this.answer = "1 es igual a 3";
      } else {
        this.answer = "ninguno se repite";
      }
    },
  },
};
</script>

<style scoped></style>
