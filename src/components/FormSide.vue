<template>
  <div id="form-side-container">
    <div>
      <FormHeader />
    </div>

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
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: start;

  .form-container {
    width: 100%;
    height: 550px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding-top: 40px;
  }
}

/* from medium breakpoint */
@media screen and (max-width: 767px) {
  #form-side-container {
    height: 100%;

    .form-container {
      height: 100vh;
      align-items: start;
    }
  }
}

/* from large breakpoint */
@media screen and (max-width: 767px) {
  #form-side-container {
    justify-content: start;
    align-items: start;
  }
}
</style>