<template>
  <div id="form-header">
    <img src="../assets/logo-ui.jpeg" alt="">
    <h6>Untitled UI</h6>
  </div>
</template>

<script>
export default {
  name: 'FormHeader',
  props: {
    //msg: String
  }
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-header {
  height: 40px;
  padding: 20px 10px;
  width: 100%;
  background-color: $white;
  display: float;

  img {
    float: left;
    width: 20px;
    height: 20px;
  }

  h6 {
    float: left;
    font-weight: 500;
    color: $black;
    margin-left: 10px;
  }
  }
</style>