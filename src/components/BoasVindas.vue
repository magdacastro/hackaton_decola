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
      <h2 class="text-h5 text-center mb-3 mt-5">Bem vindos!</h2>
      <div class="bg-imagem">
        <v-img
          class="inicio-imagem mb-4"
          style="width: 150px"
          src="https://images.vexels.com/media/users/3/127090/isolated/preview/a608267cdd6ada5e7d294c4b01c92d40-astonished-santa-claus-face-by-vexels.png"
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
<<<<<<< HEAD
  name: "BoasVindas",
=======
  name: 'App',
  data() {
    return {
      drawer: false,
      group: null,
    }
  }
>>>>>>> 6f1023977a080b91d4eefef7aafb98f0473fdb00
};
</script>
<style scoped>
<<<<<<< HEAD
=======
.bg-imagem{
  text-align: center;
}
>>>>>>> 6f1023977a080b91d4eefef7aafb98f0473fdb00
</style>
