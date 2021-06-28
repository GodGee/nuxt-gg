<template>
  <div>
    <!-- <Mynav></Mynav> -->
    学生列表页
    <ul>
      <li v-for="stu in stus" :key="stu.id">
        <nuxt-link :to="`/student/${stu.id}`">{{ stu.name }}</nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
// import Mynav from "~/components/Mynav";

export default {
  // components: {
  //   Mynav
  // },
  layout: "headerlayout",
  data() {
    return {
      stus: [
        { name: "jack1", id: 1 },
        { name: "jack2", id: 2 },
        { name: "jack3", id: 3 }
      ]
    };
  }
};
</script>

<style></style>
