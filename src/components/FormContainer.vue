<template>
    <div id="form-container" class="col-6">

        <div class="title-welcome">Welcome back, Olivia</div>

        <p class="para-welcome">Welcome back! Please enter your details.</p>

        <LogGoogleBtn />

        <div class="or-divider">or</div>

        <FormLogin />

        <p class="any-account">Don't have an account? <span>Sign up for free</span></p>
    </div>
</template>

<script>
import LogGoogleBtn from './LogGoogleBtn.vue';
import FormLogin from './FormLogin.vue';

export default {
    name: 'FormSide',
    components: {
        LogGoogleBtn,
        FormLogin,
    },
    props: {
        //msg: String
    }
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-container {
    height: 70vh;
    min-width: 215px;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 40px;

    .title-welcome {
        align-self: start;
        font-size: 25px;
        font-weight: 600;
    }

    .para-welcome {
        align-self: start;
        color: $lightgrey;
    }

    .or-divider {
        color: $lightgrey;
    }

    .any-account {
        font-size: 10px;
        color: $lightgrey;

        span {
            color: $black;
            cursor: pointer;

            &:hover {
                text-decoration: underline;
            }
        }
    }
}
</style>