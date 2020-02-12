<template>
  <section class="slide16">
    <Page>
      <Title>Качества хорошей анимации</Title>
      <Layout>
        <List :items="animationsList" class="slide16-list"/>
      </Layout>
    </Page>
  </section>
</template>

<script>
import Layout from '@/components/Layout.vue';
import List from '@/components/List.vue';
import Page from '@/components/Page.vue';
import Title from '@/components/Title.vue';

export default {
  name: 'Slide16',
  components: {
    Layout,
    List,
    Page,
    Title,
  },
  data() {
    return {
      animationsList: [
        { main: 'Ненавязчивость' },
        { main: 'Естественность' },
        { main: 'Согласованность' },
        { main: 'Чистота' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide16 {

  &-list {
    justify-self: center;
    max-width: 960px;
  }

  a {
    color: #0b52f9;
  }
}
</style>
