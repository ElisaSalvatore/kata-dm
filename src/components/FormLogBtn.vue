<template>
    <button>Log In</button>
</template>

<script>

export default {
    name: 'FormLogBtn',
    props: {
        //msg: String
    }
}
</script>

<style scoped lang="scss">
@import '@/scss/variables.scss';

button {
    width: 100%;
    height: 40px;
    background-color: $black;
    color: $white;
    border: none;
    border-radius: 5px;
    margin: 10px 0;
}

:active{
    border: 4px solid $white;
    border-radius: 10px;
}
</style>