<template>
  <div>
    调用自定义布局文件blog.vue
  </div>
</template>
<script>
export default {
  // layout: "blog"
  layout(context) {
    console.log("context: ", context);
    return "blog";
  }
};
</script>
