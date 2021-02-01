<template>
  <img class="image" src="../assets/T.png"/>
</template>

<script>
import gsap from "gsap";

export default {
  name: "LoadingScreen",

  mounted() {
    gsap.to(".image", {duration: 3, rotationX: 360, repeat: -1});
  }
}
</script>

<style scoped>
.image {
  position: fixed;
  top: 50%;
  left: 50%;
  margin-top: -50px;
  margin-left: -100px;
}
</style>