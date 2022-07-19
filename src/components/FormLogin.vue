<template>
    <div id="form-login">
        <ValidationObserver v-slot="{ handleSubmit }">
            <form @submit.prevent="handleSubmit(onSubmit)">
                <!-- valiate email -->
                <ValidationProvider name="email" rules="required|alpha" v-slot="{ errors }">
                    <div class="group-log">
                        <input type="email" v-model="email" placeholder="Email">
                        <div class="error">{{ errors[0] }}</div>
                    </div>
                </ValidationProvider>

                <!-- valiate password -->
                <ValidationProvider name="password" rules="required|max:12|min:6" v-slot="{ errors }">
                    <div class="group-log">
                        <input type="password" v-model="password" placeholder="Password">
                        <div class="error">{{ errors[0] }}</div>
                    </div>
                </ValidationProvider>

                <!-- checkbox and forgot psw -->
                <div class="options">
                    <span class="check">
                        <input type="checkbox">
                        <label for="checkbox" class="check-text">Rememeber for 30 days</label>
                    </span>
                    <span class="forgot">Forgot password</span>
                </div>

                <!-- login button -->
                <div class="login-button">
                    <FormLogBtn />
                </div>

            </form>
        </ValidationObserver>

    </div>
</template>

<script>
import FormLogBtn from './FormLogBtn.vue';

export default {
    data() {
        return {
            formData: {
                email: '',
                password: '',
                rememberData: null,
            }
        }
    },
    components: {
        FormLogBtn,
    },
    methods: {
        onSubmit() {
            console.log(this.formData);
        },
    }
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-login {
    width: fit-content;

    form {

        .group-log {
            padding: 4px 0;

            input {
                width: 100%;
                font-size: 12px;
                border: none;
                border-bottom: 1px solid $lightgrey;
                padding: 10px 0;
            }
        }

        .error {
            font-size: 12px;
            color: tomato;
            padding: 2px;
            border-radius: 5px;
        }

        .options {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;

            .check {
                display: flex;
                align-items: center;

                input {
                    margin-right: 5px;
                }

                .check-text {
                    font-size: 10px;
                    padding-right: 20px;
                }
            }

            .forgot {
                font-size: 10px;
                font-weight: 600;
                text-decoration: underline;
                cursor: pointer;
            }
        }

        .login-button {
            height: 50px;
        }
    }
}

/* mobile version */
@media screen and (max-width: 991px) {
    #form-login {
        width: 100%;
    }
}
</style>
