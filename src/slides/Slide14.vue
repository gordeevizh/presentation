<template>
  <section class="slide14">
    <Page>
      <Title>Вместо вывода - Анимации с точки зрения UX</Title>
      <h2>
        Честно украдено из доклада Ильи Бирмана&nbsp;
        <a href="https://www.youtube.com/watch?v=igcKRMBHiqE" target="_blank" noopener noreferer>“Интерфейсные анимации”</a>
      </h2>
    </Page>
  </section>
</template>

<script>
import Page from '@/components/Page.vue';
import Title from '@/components/Title.vue';

export default {
  name: 'Slide14',
  components: {
    Page,
    Title,
  },
};
</script>

<style lang="postcss" scoped>
.slide14 {
  a {
    color: #0b52f9;
  }
}
</style>
