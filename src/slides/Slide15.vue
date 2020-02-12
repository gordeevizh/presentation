<template>
  <section class="slide14">
    <Page>
      <Title>Когда использовать анимации</Title>
      <Layout>
        <List :items="animationsList" class="slide14-list"/>
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
  name: 'Slide14',
  components: {
    Layout,
    List,
    Page,
    Title,
  },
  data() {
    return {
      animationsList: [
        { main: 'Внимание' },
        { main: 'Объяснение' },
        { main: 'Реалистичность' },
        { main: 'Шоу', span: '(Должно быть безупречным)' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide14 {

  &-list {
    justify-self: center;
    max-width: 960px;
  }

  a {
    color: #0b52f9;
  }
}
</style>
