<template>
  <div
    class="main-photo"
    :style="{ 'background-image': 'url(' + image.url + ')' }"
  ></div>
</template>

<script>
import axios from "axios";

// function Image() {
//   return {
//     url: null,
//     albumId: null,
//     imageId: null
//   };
// }

class Image {
  url = null;
  albumId = null;

}

export default {
  name: "MainPhoto",

  data() {
    return {
      image: null
    }
  },

  mounted() {
    axios.get("https://aws.random.cat/meow").then(response => {
      this.image.url = response.data.file;
      this.image.albumId = "cats";
    });
  }
};
</script>

<style scoped>
.main-photo {
  width: 100%;
  height: auto;
  background-repeat: repeat-x;
  background-position: center;
  background-size: contain;
}

.main-photo::before {
  content: "";
  display: block;
  padding-bottom: 50%;
}
</style>
