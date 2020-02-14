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

    @media (max-width: 1024px) {
      flex-direction: column;
    }

    & > * {
      width: 50%;

      @media (max-width: 1024px) {
         width: 100%;
      }
    }
  }
</style>
