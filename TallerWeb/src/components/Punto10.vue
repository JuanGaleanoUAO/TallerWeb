<template>
  <h2>Ingrese la cantidad de filas (N) y columnas (M)</h2>
  <div>
    N:<input type="number" v-model="N" /> M:<input type="number" v-model="M" />
  </div>
  <h2>Matrix</h2>
  <table>
    <tr v-for="n in N" :key="n">
      <td v-for="m in M" :key="n.toString() + ',' + m.toString()">
        {{ n.toString() + "," + m.toString() }}
      </td>
    </tr>
  </table>
</template>

<script>
export default {
  data() {
    return {
      N: 0,
      M: 0,
    };
  },
};
</script>

<style scoped></style>
