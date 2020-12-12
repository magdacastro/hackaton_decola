<template>
  <div id="app">
    <Listagem/>
    <BoasVindas />
  </div>
</template>

<script>
import BoasVindas from "./components/BoasVindas.vue";
import Listagem from "./components/Listagem.vue";

export default {
  name: "App",
  components: {
    Listagem,
    BoasVindas,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
