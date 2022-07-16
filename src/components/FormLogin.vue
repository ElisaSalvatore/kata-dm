<template>
    <div id="form-login">
        <form>
            <!-- email -->
            <div class="email">
                <input type="email" placeholder="Email" required>
            </div>

            <!-- password -->
            <div class="password">
                <input type="password" placeholder="Password" required>
            </div>

            <!-- checkbox and forgot psw -->
            <div class="options">
                <span class="check">
                    <input type="checkbox">
                    <label for="checkbox">Rememeber for 30 days</label>
                </span>
                <span class="forgot">Forgot password</span>
            </div>

            <FormLogBtn />
        </form>
    </div>
</template>

<script>
import FormLogBtn from './FormLogBtn.vue';

export default {
    name: 'FormLogin',
    components: {
        FormLogBtn,
    },
    props: {
        //msg: String
    }, 
    methods: {
    
    },
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

#form-login {
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
}
</style>