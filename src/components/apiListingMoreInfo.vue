<template>
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
</template>

<script>
export default {
  data: () => ({}),
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
