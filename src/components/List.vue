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
  font-size: 3vw;
  line-height: 1.2em;
  margin: 0;
  display: block;

  @media (max-width: 1024px) {
    font-size: 5vw;
  }

  &-item {
    margin-bottom: 1em;

    @media (max-width: 1024px) {
      margin-right: 3em;
    }
  }

  &-span {
    font-size: 2.4vw;
    opacity: 0.8;

    @media (max-width: 1024px) {
      font-size: 4.4vw;
    }
  }
}
</style>
