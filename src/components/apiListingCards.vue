<template>
  <v-card class="mx-auto" max-width="344" min-height="350px">
    <v-img :src="getImageURL" height="200px"></v-img>

    <v-card-title> {{ title }} </v-card-title>

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
          <!-- <apiListingMoreInfo
            :movies="movies"
            :shortFilms="shortFilms"
            :tvShows="tvShows"
            :videoGames="videoGames"
            :parkAttractions="parkAttractions"
          /> -->
          <v-card>
            <v-list-item v-if="checkArrayLenght(movies)">
              <v-list-item-content>
                <v-list-item-title>Movies:</v-list-item-title>
                <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
                  movie
                }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-list-item two-line v-if="checkArrayLenght(shortFilms)">
              <v-list-item-content>
                <v-list-item-title>Short Films:</v-list-item-title>
                <v-list-item-subtitle
                  v-for="shortFilm of shortFilms"
                  :key="shortFilm"
                  >{{ shortFilm }}</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
            <v-list-item three-line v-if="checkArrayLenght(tvShows)">
              <v-list-item-content>
                <v-list-item-title>TV Shows:</v-list-item-title>
                <v-list-item-subtitle v-for="tvShow of tvShows" :key="tvShow">{{
                  tvShow
                }}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <v-list-item four-line v-if="checkArrayLenght(videoGames)">
              <v-list-item-content>
                <v-list-item-title>Video Games:</v-list-item-title>
                <v-list-item-subtitle
                  v-for="videoGame of videoGames"
                  :key="videoGame"
                  >{{ videoGame }}</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
            <v-list-item five-line v-if="checkArrayLenght(parkAttractions)">
              <v-list-item-content>
                <v-list-item-title>Park Attractions:</v-list-item-title>
                <v-list-item-subtitle
                  v-for="parkAttraction of parkAttractions"
                  :key="parkAttraction"
                  >{{ parkAttraction }}</v-list-item-subtitle
                >
              </v-list-item-content>
            </v-list-item>
          </v-card>
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
// import apiListingMoreInfo from "../components/apiListingMoreInfo";
export default {
  data: () => ({
    show: false,
    // return: {
    //   movies: [],
    //   shortFilms: [],
    //   tvShows: [],
    //   videoGames: [],
    //   parkAttractions: [],
    // },
  }),
  // components: {
  //   apiListingMoreInfo,
  // },
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
    },
    shortFilms: {
      type: Array,
    },
    tvShows: {
      type: Array,
    },
    videoGames: {
      type: Array,
    },
    parkAttractions: {
      type: Array,
    },
  },
  computed: {
    getImageURL() {
      return this.imageUrl;
    },
  },
  methods: {
    checkArrayLenght(something) {
      if (something.length >= 1) {
        return true;
      } else {
        return false;
      }
    },
  },
};
</script>
