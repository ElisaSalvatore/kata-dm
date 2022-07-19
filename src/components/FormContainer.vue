<template>
    <div id="form-container">

        <div class="title-welcome ">Welcome back, Olivia</div>

        <p class="para-welcome ">Welcome back! Please enter your details.</p>

        <div class="w-100">
            <LogGoogleBtn />
        </div>

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

}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-container {
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    padding: 0 10px;

    .title-welcome {
        font-size: 20px;
        align-self: start;
        font-weight: 600;
        margin: 0;
        padding: 0;
    }

    .para-welcome {
        font-size: 12px;
        align-self: start;
        color: $lightgrey;
        margin: 0;
        padding: 0;
        
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

/* from medium breakpoint */
@media screen and (max-width: 767px) {
#form-container {
        width: 100%;
        padding: 0 20px;
        justify-content: space-around;
    }

    .para-welcome {
        align-self: start;
    }
}
</style>