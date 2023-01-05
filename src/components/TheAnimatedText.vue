<script>
    import TheInputField from './TheInputField.vue';

    export default{
        components: { TheInputField },

        data() {
            return {
                text: "C:\\Users\\gab_che\\guest34230>",
            };
        },
        computed: {
            countChar() {
                return { "--steps": this.text.length };
            }
        },
}
</script>

<template>
    <label class="d-flex">
        <p :style="countChar">{{ this.text }}</p>
        <TheInputField />
    </label>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;
    @use '../styles/partials/animations' as *;

    p{
        position: relative;
        width: max-content;

        &::after,
        &::before{
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            left: 0;
            bottom: 0;
        };

        &::after{
            width: .2rem;
            background: $color_accent;
            //animation: typewriter $typewriter_speed steps(var(--steps)) $animation_delay forwards, blink .75s steps(var(--steps)) infinite;
        };

        &::before{
            animation: typewriter $typewriter_speed steps(var(--steps)) $animation_delay forwards;
            background-color: $screen_bg;
        };
    }
</style>