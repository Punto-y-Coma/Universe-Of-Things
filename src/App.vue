<template>
  <v-app>
    <!--  <v-app-bar
      app
      style="background: linear-gradient(to right, #ffaf7b, #d76d77, #3a1c71)"
      dark
      class="d-flex justify-center"
      height="100px"
    > -->

    <v-container
      style="background: linear-gradient(to right, #480848, #29215b)"
      fluid
    >
      <v-layout wrap>
        <v-flex class="d-flex justify-center" xs12>
          <v-img
            alt="Disney"
            class="shrink"
            src="./assets/disney-logo-white.png"
            width="120"
          />
        </v-flex>
        <v-flex xs4 lg5></v-flex>
        <v-flex class="white--text d-flex justify-center align-center" xs4 lg2>
          <v-flex d-flex justify-end mr-2> Personajes </v-flex>
          <v-flex d-flex justify-center> | </v-flex>
          <v-flex d-flex justify-start ml-2> Favoritos </v-flex>
        </v-flex>
        <v-flex class="d-flex justify-end" xs4 lg5>
          <v-btn
            href="https://github.com/vuetifyjs/vuetify/releases/latest"
            target="_blank"
            text
          >
            <v-icon color="white">mdi-open-in-new</v-icon>
          </v-btn>
        </v-flex>
      </v-layout>
    </v-container>

    <!-- </v-app-bar> -->

    <v-main>
      <router-view />
    </v-main>

    <v-footer
      app
      style="background: linear-gradient(to right, #29215b, #480848)"
      height="50px"
    >
      <v-layout>
        <v-flex
          class="d-flex justify-start align-center"
          text-caption
          white--text
          xs6
          sm4
          md2
          lg2
        >
          <v-flex> Terms of use </v-flex>
          <v-flex> | </v-flex>
          <v-flex> Contact </v-flex>
        </v-flex>
        <v-flex
          class="d-flex justify-end align-center"
          text-caption
          white--text
          xs6
          sm8
          md10
          lg10
        >
          Disney
        </v-flex>
      </v-layout>
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
