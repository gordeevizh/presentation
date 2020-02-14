<template>
  <section class="slide12">
    <Page>
      <SubTitle>Пример</SubTitle>
      <iframe class="frame" src="https://threejs.org/examples/#webgl_animation_skinning_blending" frameborder="0"></iframe>
    </Page>
  </section>
</template>

<script>
/* eslint-disable */
import anime from 'animejs';

import Page from '@/components/Page.vue';
import SubTitle from '@/components/SubTitle.vue';

export default {
  name: 'Slide12',
  components: {
    Page,
    SubTitle,
  },
};
</script>

<style lang="postcss" scoped>

.slide12 {
  .frame {
    width: 100vw;
    height: 75vh;
  }
}

</style>
