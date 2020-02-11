<template>
  <h1 class="title">
    <slot>Title</slot>
  </h1>
</template>

<script>
export default {
  name: 'Title',
};
</script>

<style lang="postcss" scoped>
  .title {
    font-size: 80px;
  }
</style>
