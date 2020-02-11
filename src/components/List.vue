<template>
  <ul class="list">
    <li v-for="(item, index) in items" :key="index">
      {{item.main}} <span>{{item.span}}</span>
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

<style lang="postcss" scoped>
.list {
  text-align: left;
  font-size: 36px;
  line-height: 1.5em;

  & span {
    font-size: 28px;
    opacity: 0.7;
  }
}
</style>
