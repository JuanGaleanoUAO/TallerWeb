<template>
  <div>
    <h1>Ejercicio 7</h1>
    <p>Digite 10 salarios y presione Enter</p>
    <input @keypress.enter="push()" type="number" v-model="Sal" /><br />
    <button @click="addSal()">+0.8%</button>
    <ul v-for="(item, index) in newItems">
      <li>{{ index + 1 }}: {{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Salary",
  data() {
    return {
      Sal: "",
      items: [],
      newItems: [],
    };
  },
  methods: {
    push() {
      return this.items.push(this.Sal);
    },
    addSal() {
      return (this.newItems = this.items.map((x) => x + x * 0.8));
    },
  },
};
</script>

<style scoped></style>
