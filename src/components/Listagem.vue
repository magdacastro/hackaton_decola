<template>
  <v-container>
    <div class="list">
      <v-btn
        class="btn-show"
        color="red"
        dark
        large
        elevation="2"
        @click="puxarCartas"
        >Visualizar cartas</v-btn
      >
      <!-- <button @click="puxarCartas">Trazer Cartas</button>-->
      <div v-for="carta in cartas" :key="carta.name">
        <h3 class="nome">{{ carta.name }}</h3>
        <p class="address">Endereço: {{ carta.address }}</p>
        <p class="carta">" {{ carta.description }} "</p>
        <v-btn class="btn-adote" elevation="2">Adotar esta carta</v-btn>
      </div>
    </div>
  </v-container>
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
      fetch("https://it3yui.firebaseio.com/natal.json").then((response) => {
        response.json().then((data) => {
          let CartasNovoArray = data.map((target) => {
            if (!target.address.match(/^[A-Zãáéêíîõóú\sa-z]*\s-\s/)) {
              target.address = target.address
                .match(/[A-Zãáéêíîõóú\sa-z]*$/)[0]
                .trim()
                .replace("o S", "o - S");
            }
            return target;
          });
          this.cartas = CartasNovoArray;
        });
      });

      /*fetch("https://it3yui.firebaseio.com/natal.json")
        .then((response) => response.json())
        .then((json) => {
          this.cartas = json;
        });*/
    },
  },
};
</script>

<style scoped>
.list {
  text-align: center;
}

.nome {
  margin-top: 30px;
}

.carta {
  font-style: italic;
}

.btn-adote {
  margin-bottom: 30px;
}
</style>
