<template>
  <input type="text" v-model="sec" placeholder="hora en segundos" />
  <br />
  <h2>{{ convertir }}</h2>
</template>

<script>
export default {
  name: "Hora",
  data() {
    return {
      sec: "",
    };
  },
  computed: {
    convertir() {
      return `${Math.floor(this.sec / 3600)}horas, ${Math.floor(
        this.sec / 60
      )} minutos y ${Math.round(this.sec) % 60}segundos.`;
    },
  },
};
</script>

<style scoped></style>
