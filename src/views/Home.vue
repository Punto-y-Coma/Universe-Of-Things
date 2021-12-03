<template>
  <div>
    <div v-for="character of characters" :key="character.id">
      <apiListingCards :title="character.name" :imageUrl="character.imageUrl" />
    </div>
  </div>
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
          // console.log(data);
          // console.log(data.data);
          // console.log(data.data[0]);
          // console.log(data.data[0].films);
          // console.log("test");
        });
    },
  },
  created() {
    this.loadDisneyAPI();
  },
};
</script>
