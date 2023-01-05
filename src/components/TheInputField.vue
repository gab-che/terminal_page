<script>
    export default{
        
    }
</script>

<template>
    <input type="text" name="input" id="input">
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;
    @use '../styles/partials/animations' as *;

    input{
        @include flex_grow;
        border: none;
        background-color: $screen_bg;
        color: $color_accent;

        &:active,
        &:focus,
        &:focus-visible{
            border:none;
            outline: none;
        }
    }
</style>