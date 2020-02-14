<template>
  <section
    class="home"
    tabindex="0"
    @keyup.right="showNext"
    @keyup.left="showPrev"
  >
    <SwipeChecker
      @swipeLeft="showNext"
      @swipeRight="showPrev"
    >
      <component :is="currentSlide"/>
    </SwipeChecker>
  </section>
</template>

<script>
import SwipeChecker from '@/components/SwipeChecker.vue';
import Slide1 from '@/slides/Slide1.vue';
import Slide2 from '@/slides/Slide2.vue';
import Slide3 from '@/slides/Slide3.vue';
import Slide4 from '@/slides/Slide4.vue';
import Slide5 from '@/slides/Slide5.vue';
import Slide6 from '@/slides/Slide6.vue';
import Slide7 from '@/slides/Slide7.vue';
import Slide8 from '@/slides/Slide8.vue';
import Slide9 from '@/slides/Slide9.vue';
import Slide10 from '@/slides/Slide10.vue';
import Slide11 from '@/slides/Slide11.vue';
import Slide12 from '@/slides/Slide12.vue';
import Slide13 from '@/slides/Slide13.vue';
import Slide14 from '@/slides/Slide14.vue';
import Slide15 from '@/slides/Slide15.vue';
import Slide16 from '@/slides/Slide16.vue';

export default {
  name: 'Home',
  components: {
    SwipeChecker,
    Slide1,
    Slide2,
    Slide3,
    Slide4,
    Slide5,
    Slide6,
    Slide7,
    Slide8,
    Slide9,
    Slide10,
    Slide11,
    Slide12,
    Slide13,
    Slide14,
    Slide15,
    Slide16,
  },
  data() {
    return {
      currentSlideIndex: 1,
      touch: 0,
      moved: {},
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
