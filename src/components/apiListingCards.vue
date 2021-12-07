<template>
  <v-card class="mx-auto" max-width="344" min-height="350px">
    <v-img :src="getImageURL" height="200px"></v-img>

    <v-card-title> {{ title }} </v-card-title>

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
