<template>
  <div id="form-side-container">
    <FormHeader />

    <div class="form-container">
      <FormContainer />
    </div>
    
  </div>
</template>

<script>
import FormHeader from './FormHeader.vue';
import FormContainer from './FormContainer.vue';

export default {
  name: 'FormSide',
  components: {
    FormHeader,
    FormContainer,
  },
}
</script>

<style scoped lang="scss">
#form-side-container {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;

  .form-container {
    height: 550px;
    display: flex;
    padding-top: 40px;
  }
}

/* mobile version */
@media screen and (max-width: 991px) {
#form-side-container {
    display: flex;
    flex-direction: column;
    justify-content: start;
    align-items: center;
  }
}
</style>