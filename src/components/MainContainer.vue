<template>
    <div id="main-container">
        <FormSide  class="col-12 col-lg-6"/>
        <CarouselSide class="col-6 carousel-side"/>
    </div>
</template>

<script>
import FormSide from './FormSide.vue';
import CarouselSide from './CarouselSide.vue';

export default {
    name: 'App',
    components: {
    FormSide,
    CarouselSide
}
}
</script>

<style lang="scss">
@import '@/scss/variables.scss';

#main-container {
    width: 80vw;
    height: 600px;
    max-width: 1000px;
    display: flex;
    background-color: #fff;
    color: $black;
}

/* mobile version */
@media screen and (max-width: 991px) {
#main-container {
        width: 100vw;
        height: 100vh;
    }
}
</style>
