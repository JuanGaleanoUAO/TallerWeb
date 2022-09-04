<template>
  <h1>ingrese su nombre</h1>
  <input type="text" v-model="saludo" />
  <h1>ingrese la hora</h1>
  <input type="time" v-model="hora" />
  <button @click="newMenssage">saludar</button>
  <p>{{ saludar }}</p>
</template>

<script>
export default {
  name: "saludo",
  data() {
    return {
      saludo: "",
      hora: null,
      saludar: "",
    };
  },

  methods: {
    newMenssage() {
      if (this.saludo == null) {
        this.saludar = "ingrese un nombre";
      } else {
        if (this.hora >= "6:00" && this.hora <= "11:59") {
          this.saludar = "buenos dias " + this.saludo;
          console.log("tarde" + this.saludo);
        } else if (this.hora >= "12:00" && this.hora <= "18:59") {
          this.saludar = "buenos tardes " + this.saludo;
          console.log("noches" + this.saludo);
        } else {
          this.saludar = "buenos noches " + this.saludo;
          console.log("dias" + this.saludo);
        }
      }
    },
  },
};
</script>

<style scoped></style>
