<template>
    <div class="carousel-side">
      <CarouselComponent v-for="(slide, index) in slides" 
        :key="slide" 
        :index="index" 
        :currentSlide="currentSlide"
        class="carousel-component"
      > 
        <img :src="slide" :alt="slide"> 

      </CarouselComponent>
    </div>
</template>

<script>
import CarouselComponent from './CarouselComponent.vue';

export default {
  data() {
    return {
      slides: [
        require("@/assets/slideshow/1.jpeg"),
        require("@/assets/slideshow/2.jpeg"),
        require("@/assets/slideshow/3.jpeg"),
      ],
      currentSlide: 0,
    }
  },
  components: {
    CarouselComponent,
  },
}

</script>

<style lang="scss" scoped>

  .carousel-component {
    width: 500px;
    height: 700px;
    background: tomato;

     img {
      width: 100%;
      height: 100%;
      object-fit: cover;      
    }

  }

  /* mobile version */
  @media screen and (max-width: 991px) {
    .carousel-side {
      display: none;
    }
  }
</style>