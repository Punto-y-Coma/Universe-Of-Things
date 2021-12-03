<template>
  <v-app id="inspire">
    <v-app-bar app shrink-on-scroll>
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container>
        <v-row>
          <!-- <v-col v-for="n in 10" :key="n" cols="3"> -->
          <v-col>
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
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
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
