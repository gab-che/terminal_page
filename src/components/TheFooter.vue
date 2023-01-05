<script>
    export default{}
</script>

<template>
    <footer>footer</footer>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;

    footer{
        @include border_in;
        padding: .1rem $spacer_xs;
    }
</style>