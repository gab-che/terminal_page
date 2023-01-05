<script>
    import TheHeader from './components/TheHeader.vue';
    import TheMain from './components/TheMain.vue';
    import TheFooter from './components/TheFooter.vue';

    export default {
        components: { TheHeader, TheMain, TheFooter },

        data(){
            return{
                moving: false,
                left: undefined,
                top: undefined,
            }
        },

        methods: {
            mouseDown(e, i){
                this.left = i.offsetLeft;
                this.top = i.offsetTop;
                const mouseX = e.clientX;
                const mouseY = e.clientY;
                this.moving = true;

                document.addEventListener("mousemove", (ev) => this.mouseMove(ev, mouseX, mouseY));

            },

            mouseMove(e, mouseX, mouseY){
                this.left = this.left + e.clientX - mouseX;
                this.top = this.top + e.clientY - mouseY;
            },

            mouseUp(){
                document.onmousemove = null;
                this.moving = false;
            }
        }
    }

</script>

<template>
    <div class="container">
        <div class="row py-5">
            <div class="col-11 col-md-10 col-lg-8 m-auto window"
            :style="moving ? {position: 'fixed', top: `${top}px`, left: `${left}px`} : ''"
            ref="window">
                <TheHeader @mousedown="mouseDown($event, this.$refs.window)" @mouseup="mouseUp()"/>
                <TheMain />
                <TheFooter />
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    @use './styles/general.scss';
    @use './styles/partials/variables' as *;
    @use './styles/partials/utilities' as *;
    .window{
        height: calc(100vh - 6rem);
        background-color: $window_bg;
        margin-inline: 3rem;
        padding: .25rem;
        position: relative;
        @include flex_col;
        @include border_out;
    };
</style>
