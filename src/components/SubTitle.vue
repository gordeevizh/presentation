<template>
  <h2 class="subTitle">
    <slot>subTitle</slot>
  </h2>
</template>

<script>
export default {
  name: 'SubTitle',
};
</script>

<style lang="postcss" scoped>
  .subTitle {
    font-size: 60px;
  }
</style>
