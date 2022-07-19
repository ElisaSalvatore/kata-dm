<template>
    <div class="carousel-side" col-6>
        <CarouselComponent /> 
    </div>
</template>

<script>
import CarouselComponent from './CarouselComponent.vue'

export default {
    components: {
        CarouselComponent,
    }
}
</script>

<style lang="scss" scoped>
.carousel-side {
    height: 100vh;
    // display: flex;
    // justify-content: center;
    // align-items: center;
}

/* mobile version */
@media screen and (max-width: 575px) {
    .carousel-side {
        display: none;
    }
}

</style>