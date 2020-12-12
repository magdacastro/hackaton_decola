<template>
  <v-app>
    <v-app-bar app color="red" dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title> Noel Online </v-toolbar-title>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="green--text text--lighten-2"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Início </v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Cartinhas </v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-container>
      <h2 class="text-center mb-3 mt-5" style="font-size: 45px">Bem vindos!</h2>
      <div class="bg-img">
        <v-img
          class="inicio-imagem"
          style="width: 300px; right: -450px; margin-bottom: 25px"
          src="../assets/images/noel.png"
        >
        </v-img>
      </div>
      <p>
        Você já pensou em fazer algo impactante nesse natal mesmo a distância?
        Existem muitas crianças escrevendo para o bom velhinho sobre tudo que
        desejam e esperaram o ano todo. Convido você a ter a experiência de
        adotar um sonho e ajudar a realizá-lo para a criação um Natal mais
        completo e feliz. Seja participante! Selecione entre as cartas abaixo e
        seja o tão desejado Papai Noel de uma criança.
      </p>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      drawer: false,
      group: null,
    };
  },
};
</script>

<style scoped>
/* */
</style>
