<template>
    <div class="carousel-side ">
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
    height: 90vh;
}

/* mobile version */
@media screen and (max-width: 991px) {
    .carousel-side {
        display: none;
    }
}
</style>