<template>
  <div class="slider-side-container">
    <h1>Slider side</h1>

  </div>
</template>

<script>
export default {
  name: 'SliderSide',
  props: {
    //msg: String
  }
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

.slider-side-container {
  background-color: cadetblue;
}

/* mobile version */
@media screen and (max-width: 991px) {
  .slider-side-container {
    display: none;
  }
}
</style>