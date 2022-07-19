<template>
  <div id="app">
    <MainContainer class="main-container"/>
  </div>
</template>

<script>
import MainContainer from './components/MainContainer.vue';

export default {
  name: 'App',
  components: {
    MainContainer,
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;300;400;500;600;700;800;900&display=swap');
@import '@/scss/variables.scss';

#app {
  font-family: 'Montserrat', sans-serif;
  width: 100vw;
  height: 100vh;
  margin: 0 auto;
  
}

@media screen and (min-width: 1290px) {
  #app{
    width: 1200px;
    height: 600px;
    display: flex;
    align-content: center;
    justify-content: center;
   
  }
}

</style>
