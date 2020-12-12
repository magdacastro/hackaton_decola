<template>
  <div>
    <button @click="puxarCartas">Trazer Cartas</button>
    <div v-for="carta in cartas" :key="carta.name">
      <p>Criança: {{ carta.name }}</p>
      <p>Endereço: {{ carta.address }}</p>
      <p>Carta: {{ carta.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Listagem",
  data() {
    return {
      cartas: {},
    };
  },
  methods: {
    puxarCartas() {
      fetch("https://it3yui.firebaseio.com/natal.json")
        .then((response) => response.json())
        .then((json) => {
          this.cartas = json;
        });
    },
  },
};
</script>

<style scoped>
</style>
