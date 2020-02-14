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
    font-size: 3.5vw;
    margin: 2vw 1vw;

    @media (max-width: 1024px) {
      font-size: 7vw;
      margin: 7vw 1vw;
    }
  }
</style>
