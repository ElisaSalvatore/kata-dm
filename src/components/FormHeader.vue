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
  align-content: center;
  padding: 40px 0 0 20px;

  img {
    align-self: center;
    width: 25px;
    height: 25px;
  }

  h6 {
    font-weight: 500;
    color: $black;
    padding-left: 10px;
  }
}

/* mobile version */
@media screen and (max-width: 991px) {
  h6 {
    display: none;
  }
}
</style>