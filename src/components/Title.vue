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
    font-size: 6vw;
    margin: 4vw 1vw;

    @media (max-width: 1024px) {
      font-size: 10vw;
      margin: 5vw 1vw;
    }
  }
</style>
