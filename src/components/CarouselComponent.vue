<template>
    <div v-show="currentSlide === index" class="carosuel">
        <slot></slot>
<!--         
        <button class="next">Next</button>
        <button class="prev">Prev</button> -->
    </div>
   
</template>

<script>
export default {
    props: [
        'currentSlide', 
        'index'
    ],
    data(){
        return {
        
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/scss/variables.scss';

    //.carousel {
    //     position: relative;
    //     width: 600px;
    //     height: 350px;
    //     overflow: hidden;
    // }

    // button {
    //     position: absolute;
    //     height: 40px;
    //     width: 50px;
    //     bottom: calc(50% - 20px);
    //     // border: 2px solid $white;
    //     // border-radius: 50%;
    //     background-color: red;

    //     .next {
    //         right: 0;
    //     }

    //     .prev {
    //         left: 0;
    //     }
    // }


    
</style>