<template>
    <div id="main-container">
        <FormSide  />
        <CarouselSide />
    </div>
</template>

<script>
import FormSide from './FormSide.vue';
import CarouselSide from './CarouselSide.vue';

export default {
    name: 'App',
    components: {
        FormSide,
        CarouselSide,
    }
}
</script>

<style lang="scss">
@import '@/scss/variables.scss';

#main-container {
    width: 80vw;
    max-width: 1000px;
    height: 700px;
    max-height: 700px;
    display: flex;
    text-align: center;
    justify-content: center;
    background-color: #fff;
    color: $black;
}
</style>
