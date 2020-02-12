<template>
  <section class="slide5">
    <Page>
      <SubTitle>Плюсы</SubTitle>
      <Layout>
        <List :items="pluses" class="slide5-list"/>
      </Layout>
      <SubTitle>Минусы</SubTitle>
      <Layout>
        <List :items="minuses" class="slide5-list"/>
      </Layout>
      <Layout>
        <section class="slide5-conclusion">
          <h2>
            По возможности стоит выбрирать именно этот вид анимаций,
            или совместно с JS для добавления гибкости
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
  name: 'Slide5',
  components: {
    Layout,
    List,
    Page,
    SubTitle,
  },
  data() {
    return {
      pluses: [
        { main: 'Простые', span: 'Очень просто делаются простые анимации. Просты в изучении' },
        {
          main: 'Быстрые',
          span: 'Не создают большой нагрузки на процессор (могут рендериться на GPU)',
        },
        { main: 'Достаточно хорошая поддержка браузерами' },
      ],
      minuses: [
        { main: 'Недостаточно гибкие для сложных анимаций', span: '(движения ограничены только шагами и кривой безье)' },
        {
          main: 'Можно изменять только свойства элементов',
          span: '(нельзя создавать, уничтожать)',
        },
        {
          main: 'Нельзя привязать без JS к событиям на странице',
          span: '(например анимация при прокрутке страницы)',
        },
      ],
    };
  },
};
</script>

<style lang="postcss">
.slide5 {
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
