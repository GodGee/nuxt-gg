<template>
  <div>这是{{ $route.params.id }}的个人信息</div>
</template>
<script>
export default {
  validate(obj) {
    return /^\d+$/.test(obj.params.id);
  }
};
</script>
