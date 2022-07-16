<template>
    <div id="main-container">
        <FormSide class="col-12 col-md-6" />
        <SliderSide class="col-6" />
    </div>
</template>

<script>
import FormSide from './FormSide.vue';
import SliderSide from './SliderSide.vue';

export default {
    name: 'App',
    components: {
        FormSide,
        SliderSide,
    }
}
</script>

<style lang="scss">
@import '@/scss/variables.scss';

#main-container {
    width: 80vw;
    height: 90vh;
    display: flex;
    text-align: center;
    justify-content: center;
    color: $black;
}
</style>
