<template>
  <div class="movie-hearder">
    <ul>
      <li>
        <nuxt-link to="/movie/in_theaters">正在热映</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/movie/coming_soon">即将上映</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/movie/top250">top250</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.movie-hearder {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
}
ul {
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 15px 0;
  background-color: gray;
  margin: 0;
}
li {
  line-height: 30px;
  height: 30px;
  list-style: none;
}
</style>
