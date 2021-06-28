<template>
  <div><button @click="handleVuePlugin">使用 Vue 插件</button></div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    handleVuePlugin() {
      this.$notify({ group: "all", text: "Heyy !!!" });
    }
  }
};
</script>

<style></style>
