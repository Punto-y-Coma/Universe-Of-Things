<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
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
        <v-btn elevation="2"></v-btn>
      </div>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
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
