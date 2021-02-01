<template>
  <p>{{ list }}</p>
</template>

<script>
import axios from "axios";

export default {
  name: "LoadAlbums",

  data() {
    return {
      list: null,
      isLoaded: false
    };
  },

  mounted() {
    axios.get("https://dog.ceo/api/breeds/list/all").then(response => {
      this.list = response.data.message;
    });
  }
};
</script>
