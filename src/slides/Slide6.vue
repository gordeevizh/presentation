<template>
  <section class="slide6">
    <Page>
      <Title>JS анимации</Title>
      <SubTitle>Особенности</SubTitle>
      <Layout>
        <List :items="animationsList" class="slide6-list"/>
      </Layout>
    </Page>
  </section>
</template>

<script>
import Layout from '@/components/Layout.vue';
import List from '@/components/List.vue';
import Page from '@/components/Page.vue';
import SubTitle from '@/components/SubTitle.vue';
import Title from '@/components/Title.vue';

export default {
  name: 'Slide6',
  components: {
    Layout,
    List,
    Page,
    SubTitle,
    Title,
  },
  data() {
    return {
      animationsList: [
        { main: 'Позволяют анимировать практически все' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide6 {
  &-list {
    justify-self: center;
    max-width: 960px;
  }
}
</style>
