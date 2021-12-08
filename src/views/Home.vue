<template>
  <v-app id="inspire" style="background: #212121">
    <v-container>
      <v-row>
        <v-col v-for="character in characters" :key="character.id" xs6 md4 lg3>
          <apiListingCards
            :title="character.name"
            :imageUrl="character.imageUrl"
          />
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import apiListingCards from "../components/apiListingCards";

export default {
  name: "Home",
  data() {
    return {
      characters: [],
    };
  },
  components: {
    apiListingCards,
  },
  methods: {
    loadDisneyAPI() {
      var url = "https://api.disneyapi.dev/characters";
      return fetch(url)
        .then((res) => res.json())
        .then((data) => {
          this.characters = data.data;
        });
    },
  },
  created() {
    this.loadDisneyAPI();
  },
};
</script>
