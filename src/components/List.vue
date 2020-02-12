<template>
  <ul class="list">
    <li v-for="(item, index) in items" :key="index" class="list-item">
      {{item.main}} <span class="list-span">{{item.span && item.span}}</span>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'List',
  props: {
    items: {
      default: [
        {
          main: 'Main text',
          span: 'span text',
        },
      ],
    },
  },
};
</script>

<style lang="postcss">
.list {
  text-align: left;
  font-size: 40px;
  line-height: 1.2em;

  &-item {
    margin-bottom: 1em;
  }

  &-span {
    font-size: 32px;
    opacity: 0.8;
  }
}
</style>
