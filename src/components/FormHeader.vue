<template>
  <div id="form-header">
    <img src="../assets/logo.svg" alt="">
    <h6>Untitled UI</h6>
  </div>
</template>

<script>
export default {
  name: 'FormHeader',
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-header {
  height: 50px;
  width: 100%;
  background-color: $white;
  display: flex;
  justify-content: start;
  align-items: center;

  img {
    margin: 0 10px;
    width: 25px;
    height: 25px;
  }

  h6 {
    padding-top: 10px;
    color: $black;
  }
}

/* from large breakpoint */
@media screen and (max-width: 767px) {

  h6 {
    display: none;
  }
}
</style>