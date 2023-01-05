<script>
    export default{}
</script>

<template>
    <div class="bottom_header">
        <ul class="list-unstyled d-flex">
            <li>link</li>
            <li>link</li>
            <li>link</li>
        </ul>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;

    .bottom_header{
        padding: $spacer_xs $spacer_md;
    }
</style>