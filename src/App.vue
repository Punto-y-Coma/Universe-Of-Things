<template>
  <v-app>
    <v-app-bar
      app
      style="background: linear-gradient(to right, #ffaf7b, #d76d77, #3a1c71)"
      dark
    >
    <v-div class="d-flex column">
      <div class="d-flex align-center">
        <v-img
          alt="Disney"
          class="shrink mr-6"
          contain
          src="./assets/disney-logo-white.png"
          transition="scale-transition"
          width="100"
        />
      </div>
      <div class="d-flex row">
        <p>Personajes</p>
        <p>Favoritos</p>
      </div>
    </v-div>

      <!-- <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div> 

      <v-spacer></v-spacer>-->

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">BUSCAR PERSONAJE</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>

    <v-footer
      app
      style="background: linear-gradient(to right, #ffaf7b, #d76d77, #3a1c71)"
      dark
      height="50px"
    >
      <v-spacer></v-spacer>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
