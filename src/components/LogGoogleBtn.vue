<template>
    <div>
        <button>
            <span class="log-image">
                <img src="../assets/google.svg" alt="logo">
            </span>
            <span class="log-text">
                Log in with Google
            </span>
        </button>
    </div>
</template>

<script>

export default {
    name: 'LogGoogleBtn',
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

button {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 5px 10px;
    border: 1px solid #ccc;
    border-radius: 10px;
    background-color: #fff;

    .log-image {
        width: 20px;
    }

    .log-text {
        padding: 0 10px;
        font-size: 15px;;
        font-weight: 400;
    }


    &:hover {
        background-color: $lightgrey;
        border-radius: 15px;
        color: #fff;
    }

    &:active {
        border: 1px solid $darkgrey;
        border-radius: 15px;
    }
}
</style>