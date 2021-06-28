<template>
  <div class="movie-layout">
    <movie-header> </movie-header>
    <nuxt />
  </div>
</template>

<script>
import MovieHeader from "../components/MovieHeader.vue";
export default {
  components: {
    MovieHeader
  }
};
</script>

<style scoped>
.movie-layout {
  padding-top: 50px;
}
</style>
