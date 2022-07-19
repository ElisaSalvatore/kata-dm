<template>
    <div id="main-container">
        <FormSide  class="col-12 col-md-5 col-xl-6"/>

        <CarouselSide class="col-md-7 col-xl-6 carousel-side"/>
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
    width: 100vw;
    height: 90vh;
    display: flex;
    color: $black;
}

</style>
