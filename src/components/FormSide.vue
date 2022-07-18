<template>
    <div id="form-side-container">
        <FormHeader />
        <FormContainer />
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
  props: {
    //msg: String
  }
}
</script>

<style scoped lang="scss">

  #form-side-container {
    width: 500px;
    max-height: 650px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;

  }
</style>