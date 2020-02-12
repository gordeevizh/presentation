<template>
  <section class="slide2">
    <Page>
      <Title>Виды анимаций</Title>
      <Layout>
        <List :items="animationsList" class="slide2-list"/>
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
  name: 'Slide2',
  components: {
    Layout,
    List,
    Page,
    Title,
  },
  data() {
    return {
      animationsList: [
        { main: 'CSS', span: 'анимации свойств объектов DOM, или SVG элементов' },
        { main: 'JavaScript', span: 'анимации напрямую DOM(объектной моделью документа) или SVG' },
        { main: 'Canvas', span: '(2d и 3d анимации)' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide2 {
  &-list {
    justify-self: center;
    max-width: 960px;
  }
}
</style>
