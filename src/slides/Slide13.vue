<template>
  <section class="slide13">
    <Page>
      <h2 class="slide13-conclusion">Плюсы</h2>
      <Layout>
        <List :items="pluses" class="slide13-list"/>
      </Layout>
      <h2 class="slide13-conclusion">Минусы</h2>
      <Layout>
        <List :items="minuses" class="slide13-list"/>
      </Layout>
      <h2 class="slide13-conclusion">Когда применяются</h2>
      <Layout>
        <List :items="conclusion" class="slide13-list"/>
      </Layout>
    </Page>
  </section>
</template>

<script>
import Layout from '@/components/Layout.vue';
import List from '@/components/List.vue';
import Page from '@/components/Page.vue';

export default {
  name: 'Slide13',
  components: {
    Layout,
    List,
    Page,
  },
  data() {
    return {
      pluses: [
        { main: 'Быстрые', span: 'Хорошо оптимизированы для отрисовке при помощи GPU' },
        { main: 'Позволяют анимировать 2D и 3D графику' },
      ],
      minuses: [
        { main: 'Очень сложны в реализации' },
        {
          main: 'Сложны для изучения',
        },
        {
          main: 'Реализуются в своей “песочнице”, не позволяя взаимодействовать с другими элементами DOM',
        },
      ],
      conclusion: [
        { main: 'Когда требуется анимировать множество(сотни, или тысячи) объектов' },
        {
          main: 'Для анимирования 3D объектов и для создания игр',
        },
        { main: 'Когда не нужно взаимодействие с DOM' },
        { main: 'В случаях когда не удалось подобрать технологию лучше' },
      ],
    };
  },
};
</script>

<style lang="postcss">
.slide13 {
  &-list {
    justify-self: center;
    max-width: 600px;
    font-size: 20px;

    & .list-span {
      font-size: 18px;
    }
  }

  &-conclusion {
    width: 100%;
    justify-self: center;
  }
}
</style>
