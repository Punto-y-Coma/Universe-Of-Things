<template>
  <v-card
    class="mx-auto"
    min-width="163"
    max-width="243"
    height="350"
    elevation="15"
  >
    <v-img
      src="https://static.wikia.nocookie.net/disney/images/6/61/Olu_main.png"
      height="200"
      min-width="163"
      max-width="243"
    ></v-img>

    <!--     <v-img
      src="https://images.cdn2.buscalibre.com/fit-in/360x360/0a/2b/0a2b5b51d9042a90bc7503b918eb58bf.jpg"
      lazy-src="https://yt3.ggpht.com/ytc/AKedOLTvdyXx_BMV1NliJxVqzs5kzn6XtGmYlEXb1_rmIA=s900-c-k-c0x00ffffff-no-rj"
      height="200"
      min-width="163"
      max-width="243"
    ></v-img> -->

    <v-card-title> {{ title }} </v-card-title>
    <v-card-subtitle> {{ imageUrl }} </v-card-subtitle>

    <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle>

    <v-card-actions>
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    show: false,
  }),
  props: {
    title: {
      type: String,
      required: true,
    },
    imageUrl: {
      type: String,
      required: true,
    },
  },
  computed: {
    getImageURL() {
      return this.imageUrl;
    },
  },
};
</script>
