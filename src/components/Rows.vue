<template>
  <section class="rows">
    <slot></slot>
  </section>
</template>

<script>
export default {
  name: 'Rows',
};
</script>

<style lang="postcss" scoped>
  .rows {
    display: flex;
    position: relative;

    & > * {
      width: 50%;
    }
  }
</style>
