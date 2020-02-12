<template>
  <section class="slide9">
    <Page>
      <SubTitle>Плюсы</SubTitle>
      <Layout>
        <List :items="pluses" class="slide9-list"/>
      </Layout>
      <SubTitle>Минусы</SubTitle>
      <Layout>
        <List :items="minuses" class="slide9-list"/>
      </Layout>
      <Layout>
        <section class="slide9-conclusion">
          <h2>
            Используются когда нужно сделать что-то сложное, интересное (что-то для вау-эффекта)
          </h2>
        </section>
      </Layout>
    </Page>
  </section>
</template>

<script>
import Layout from '@/components/Layout.vue';
import List from '@/components/List.vue';
import Page from '@/components/Page.vue';
import SubTitle from '@/components/SubTitle.vue';

export default {
  name: 'Slide9',
  components: {
    Layout,
    List,
    Page,
    SubTitle,
  },
  data() {
    return {
      pluses: [
        { main: 'Гибкие', span: 'В них может присутствовать любая анимационная логика' },
        {
          main: 'Можно использовать вместе с различными событиями',
        },
        { main: 'Можно управлять сразу группой элементов' },
      ],
      minuses: [
        { main: 'Более требовательны к процессорной мощности' },
        {
          main: 'Требуют подключения дополнительных библиотек и/или написания кода',
        },
        {
          main: 'Сложнее для реализации',
        },
        {
          main: 'Не работают с отключенным JS на странице',
        },
      ],
    };
  },
};
</script>

<style lang="postcss">
.slide9 {
  &-list {
    justify-self: center;
    max-width: 960px;
    font-size: 20px;

    & .list-span {
      font-size: 18px;
    }
  }

  &-conclusion {
    width: 100%;
    justify-self: center;
    max-width: 960px;
  }
}
</style>
