<template>
  <v-app>
    <v-app-bar
      style="background: linear-gradient(to right, #480848, #29215b)"
      fluid
      app
      height="100"
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
          <div>|</div>
          <v-flex d-flex justify-start ml-2> Favoritos </v-flex>
        </v-flex>
        <v-flex class="d-flex justify-end" xs4 lg5>
          <v-btn
            href="https://github.com/vuetifyjs/vuetify/releases/latest"
            target="_blank"
            text
          >
            <v-icon color="white">mdi-magnify</v-icon>
          </v-btn>
        </v-flex>
      </v-layout>
    </v-app-bar>

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
        >
          <div class="mx-2">Terms of use</div>
          <div>|</div>
          <div class="mx-2">Contact</div>
        </v-flex>
        <v-flex
          class="d-flex justify-end align-center"
          text-caption
          white--text
          xs6
        >
          © Disney
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
  mounted() {},
  methods: {
    loadDisneyAPI() {
      var url = "https://api.npms.io/v2/search?q=vue";
      return fetch(url)
        .then((res) => res.json())
        .then((data) => {
          this.products = data;
          console.log(this.products);
        });
      // fetch(url)
      //   .then((response) => response.json())
      //   .then((data) => (this.totalVuePackages = data.total));
      // console.log("testestestestestestestest");
    },
  },
};
</script>
