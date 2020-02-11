<template>
  <div class="page">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Page',
};
</script>

<style lang="postcss" scoped>
.page {
  background-color: #f9d30b;
  width: 100%;
  height: 100%;
  display: block;
  position: absolute;
  overflow: hidden;
}
</style>
