<template>
  <h1>minutos</h1>
  <span>{{ minutominimo }}</span
  ><br />
  <input type="text" v-model="minutos" />
  <span>{{ minutos }}-{{ minutosextra }}={{ cantidadminutosextras }}</span
  ><br />
  <span>{{ valorminutobase }}+{{ minutosextra }}={{ getsuma }}</span
  ><br />
  <span
    >{{ minutosextra }}*{{ cantidadminutosextras }}={{
      getmultiplicacion
    }}</span
  ><br />
  <h2 v-if="minutos > 3">{{ operaciones }}</h2>
  <h2 v-else>{{ minutos }}total a pagar:100</h2>
</template>

<script>
export default {
  name: "minutos",
  data() {
    return {
      minutominimo: 3,
      minutosextra: 3,
      valorminutobase: 100,
      cantidadminutosextras: 50,
      minutos: "",
    };
  },
  computed: {
    operaciones() {
      console.log("calling method");
      return `${Math.floor(
        this.minutos - this.minutosextra
      )}cantidad de minutos extras, ${Math.floor(
        (this.minutos - this.minutosextra) * this.cantidadminutosextras
      )} valor extra, ${Math.round(
        this.valorminutobase +
          (this.minutos - this.minutosextra) * this.cantidadminutosextras
      )}valor total.`;
    },
  },
};
</script>

<style scoped></style>
