<template>
  <v-card class="mx-auto" max-width="344" min-height="350px">
    <v-img :src="getImageURL" height="200px"></v-img>

    <v-card-title> {{ title }} </v-card-title>

    <!-- <v-card-subtitle> 1,000 miles of wonder </v-card-subtitle> -->

    <v-card-actions>
      <v-btn color="orange lighten-2" text> More info </v-btn>

      <v-spacer></v-spacer>

      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>
    </v-card-actions>
    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          <apiListingMoreInfo :movies="movies" />
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
import apiListingMoreInfo from "../components/apiListingMoreInfo";
export default {
  data: () => ({
    show: false,
  }),
  components: {
    apiListingMoreInfo,
  },
  props: {
    title: {
      type: String,
      required: true,
    },
    imageUrl: {
      type: String,
      required: true,
    },
    movies: {
      type: Array,
      required: false,
    },
  },
  computed: {
    getImageURL() {
      return this.imageUrl;
    },
  },
};
</script>
