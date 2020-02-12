<template>
  <section
    class="home"
    tabindex="0"
    @keyup.right="showNext"
    @keyup.left="showPrev"
  >
    <component :is="currentSlide"/>
  </section>
</template>

<script>
import Slide1 from '@/slides/Slide1.vue';
import Slide2 from '@/slides/Slide2.vue';
import Slide3 from '@/slides/Slide3.vue';

export default {
  name: 'Home',
  components: {
    Slide1,
    Slide2,
    Slide3,
  },
  data() {
    return {
      currentSlideIndex: 1,
    };
  },
  computed: {
    currentSlide() {
      return `Slide${this.currentSlideIndex}`;
    },
  },
  methods: {
    showNext() {
      this.currentSlideIndex += 1;
    },
    showPrev() {
      this.currentSlideIndex -= 1;
    },
  },
};
</script>
