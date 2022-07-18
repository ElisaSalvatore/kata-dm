<template>
    <div>
        <form @submit.prevent="handleSubmit">
            <!-- email -->
            <div class="email">
                <input type="email" placeholder="Email" v-model="email" required>
            </div>

            <!-- password -->
            <div class="password">
                <input type="password" placeholder="Password" v-model="password" required >
            </div>
            <!-- if password error -->
            <div v-if="passwordError" class="error"> {{passwordError}} </div>
            
            <!-- checkbox and forgot psw -->
            <div class="options">
                <span class="check">
                    <input type="checkbox">
                    <label for="checkbox">Rememeber for 30 days</label>
                </span>
                <span class="forgot">Forgot password</span>
            </div>

            <!-- login button -->
            <div class="login-button">
                <FormLogBtn />
            </div>
            
        </form>
    </div>
</template>

<script>
import FormLogBtn from './FormLogBtn.vue';

export default {
    name: 'FormLogin',
    data() {
        return {
            email: '',
            password: '',
            passwordError: '',
        }
    },
    components: {
        FormLogBtn,
    },
    methods: {
        handleSubmit() {
            // validate password
            this.passwordError = this.password.length > 6 ? '' : 'La password deve essere di minimo 6 caratteri.';

            if (!this.passwordError) {
                console.log(`email: ${this.email}`);
                console.log(`password: ${this.password}`);
            }
        },
    },
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

form {    
    .email {
        padding: 5px 0;

        input {
            width: 100%;
            border: none;
            border-bottom: 1px solid $lightgrey;
            padding: 10px 0;

        }
    }

    .password {
        padding: 5px 0;

        input {
            width: 100%;
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
            align-self: center;

            input {
                margin-right: 5px;
            }

            label {
                font-size: 10px;
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
</style>