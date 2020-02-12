<template>
  <section class="slide10">
    <Page>
      <Title>Анимации на Canvas</Title>
      <SubTitle>Особенности</SubTitle>
      <Layout>
        <List :items="animationsList" class="slide10-list"/>
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
  name: 'Slide10',
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
        { main: 'Создаются с помощью JS на холсте фиксированного размера' },
      ],
    };
  },
};
</script>

<style lang="postcss" scoped>
.slide10 {
  &-list {
    justify-self: center;
    max-width: 960px;
  }
}
</style>
