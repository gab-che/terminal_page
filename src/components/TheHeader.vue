<script>
    import TheTopHeader from './TheTopHeader.vue';
    import TheBottomHeader from './TheBottomHeader.vue';

    export default { 
            components: { TheTopHeader, TheBottomHeader } 
        }
</script>

<template>
    <header>
        <TheTopHeader />
        <TheBottomHeader />
    </header>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;
</style>