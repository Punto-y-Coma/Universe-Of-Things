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
        <v-list-item-title>Movies:</v-list-item-title>
        <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
          movie
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-list-item three-line>
      <v-list-item-content>
        <v-list-item-title>Movies:</v-list-item-title>
        <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
          movie
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-list-item four-line>
      <v-list-item-content>
        <v-list-item-title>Movies:</v-list-item-title>
        <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
          movie
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
    <v-list-item five-line>
      <v-list-item-content>
        <v-list-item-title>Movies:</v-list-item-title>
        <v-list-item-subtitle v-for="movie of movies" :key="movie">{{
          movie
        }}</v-list-item-subtitle>
      </v-list-item-content>
    </v-list-item>
  </v-card>
</template>

<script>
export default {
  data: () => ({}),
  movies: {
    type: Array,
    required: false,
  },
};
</script>
