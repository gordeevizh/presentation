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
import Slide4 from '@/slides/Slide4.vue';
import Slide5 from '@/slides/Slide5.vue';
import Slide6 from '@/slides/Slide6.vue';
import Slide7 from '@/slides/Slide7.vue';
import Slide8 from '@/slides/Slide8.vue';

export default {
  name: 'Home',
  components: {
    Slide1,
    Slide2,
    Slide3,
    Slide4,
    Slide5,
    Slide6,
    Slide7,
    Slide8,
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
