<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 255 255" role="img">
    <g transform="translate(128, 128)">
      <circle
        :class="animating ? 'circle-animating' : ''"
        r="128"
        fill="rgb(25,25,25)"/>
    </g>
    <path d="M0 0v256h256V0H0zm128 16a56.042 56.042 0 0 1 56.043 56.043v56.465a69.883 69.883 0 0 1 13.84 41.61A69.883 69.883 0 0 1 128 240a69.883 69.883 0 0 1-69.883-69.883 69.883 69.883 0 0 1 13.84-41.623V72.043A56.042 56.042 0 0 1 128 16zm0 14.01a42.032 42.032 0 0 0-42.031 42.033v42.353A69.883 69.883 0 0 1 128 100.232a69.883 69.883 0 0 1 42.031 14.137V72.043A42.032 42.032 0 0 0 128 30.01zm-7.006 91.07v7.6a42.032 42.032 0 0 0-35.025 41.437A42.032 42.032 0 0 0 128 212.148a42.032 42.032 0 0 0 42.031-42.03 42.032 42.032 0 0 0-35.025-41.4v-7.638h-14.012zm0 21.016h14.012v8.23a21.016 21.016 0 0 1 14.01 19.791A21.016 21.016 0 0 1 128 191.133a21.016 21.016 0 0 1-21.016-21.016 21.016 21.016 0 0 1 14.01-19.787v-8.234z" fill="#fff"/>
  </svg>
</template>

<script>
export default {
  name: 'fancy-logo',

  data() {
    return { animating: false };
  },

  mounted() {
    this.animating = true;
  },

  destroyed() {
    this.animating = false;
  },
};
</script>

<style scoped>
circle {
  transform: scale(0);
  transition: transform 1.25s;
}

circle.circle-animating {
  transform: scale(1);
}
</style>
