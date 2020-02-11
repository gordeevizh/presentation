<template>
  <section class="slide1">
    <Page>
      <h1>Animations</h1>
    </Page>
  </section>
</template>

<script>
import Page from '@/components/Page.vue';

export default {
  name: 'Slide1',
  components: {
    Page,
  },
};
</script>

<style lang="postcss" scoped>

.slide1 {
  & h1 {
    font-size: 20vw;
    display: inline-block;
    margin-left: -0.2em;
  }
}

</style>
