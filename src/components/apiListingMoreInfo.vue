<template>
  <v-card>
    <v-list-item>
      <v-list-item-content>
        <v-list-item-title>Movies:</v-list-item-title>
        <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
          movie
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-list-item two-line>
      <v-list-item-content>
        <v-list-item-title>Short Films:</v-list-item-title>
        <v-list-item-subtitle
          v-for="shortFilm of shortFilms"
          :key="shortFilm"
          >{{ shortFilm }}</v-list-item-subtitle
        >
      </v-list-item-content>
    </v-list-item>
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title>TV Shows:</v-list-item-title>
        <v-list-item-subtitle v-for="tvShow of tvShows" :key="tvShow">{{
          tvShow
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-list-item four-line>
      <v-list-item-content>
        <v-list-item-title>Video Games:</v-list-item-title>
        <v-list-item-subtitle
          v-for="videoGame of videoGames"
          :key="videoGame"
          >{{ videoGame }}</v-list-item-subtitle
        >
      </v-list-item-content>
    </v-list-item>
    <v-list-item five-line>
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
};
</script>
