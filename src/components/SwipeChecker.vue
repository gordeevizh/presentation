<template>
  <div
    @touchstart="updateStartPosition"
    @touchend="updateEndPosition"
  >
    <slot></slot>
  </div>
</template>

<script>

function getPoint(event) {
  return { x: event.changedTouches[0].pageX, y: event.changedTouches[0].pageY };
}

export default {
  name: 'SwipeChecker',
  props: {
    distance: {
      default: 100,
      type: Number,
    },
  },
  data() {
    return {
      startPosition: {
        x: null,
        y: null,
      },
      endPosition: {
        x: null,
        y: null,
      },
    };
  },
  watch: {
    endPosition(value) {
      const distanceX = +value.x - this.startPosition.x;
      const distanceY = +value.y - this.startPosition.y;

      if (distanceX > this.distance) {
        this.$emit('swipeRight');
      }

      if (distanceX < -this.distance) {
        this.$emit('swipeLeft');
      }

      if (distanceY > this.distance) {
        this.$emit('swipeBottom');
      }

      if (distanceY < -this.distance) {
        this.$emit('swipeTop');
      }
    },
  },
  methods: {
    updateStartPosition(e) {
      this.startPosition = getPoint(e);
    },
    updateEndPosition(e) {
      this.endPosition = getPoint(e);
    },
  },
};
</script>
