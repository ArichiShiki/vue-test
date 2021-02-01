<template>
  <div class="about">
    <!-- <h1>This is an about page</h1>
    <LoadAlbums/> -->
    <LoadingScreen/>
  </div>
</template>

<script>
// import LoadAlbums from "@/components/LoadAlbums.vue";
import LoadingScreen from '@/components/LoadingScreen.vue';

export default {
  name: "About",
  components: {
    // LoadAlbums,
    LoadingScreen
  }
}
</script>