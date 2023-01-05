<script>
    import TheAnimatedText from './TheAnimatedText.vue';
    export default{
        components: { TheAnimatedText }
    }
</script>

<template>
    <main>
        <p>Copyright (C) gab_che. All rights reserved.</p>
        <p>Type 'ls' to see list of available commands.</p>
        <TheAnimatedText />
    </main>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;

    main{
        @include flex_grow;
        @include border_in;
        margin-bottom: .15rem;
        background-color: $screen_bg;
        color: $color_accent;
        font-family: 'Source Code Pro', monospace;
        padding: $spacer_md;
    }
</style>