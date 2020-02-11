<template>
  <section class="layout">
    <slot></slot>
  </section>
</template>

<script>
export default {
  name: 'Layout',
};
</script>

<style lang="postcss" scoped>
  .layout {
    display: grid;
    position: relative;
  }
</style>
