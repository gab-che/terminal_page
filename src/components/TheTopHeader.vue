<script>
    export default{
        data(){
            return{
                iconList: ['fa-window-minimize', 'fa-window-maximize', 'fa-xmark']
            }
        }
    }
</script>

<template>
    <div class="top_header">
        <div class="left_header d-flex align-items-center">
            <div class="folder_icon">
                <i class="fa-solid fa-terminal"></i>
            </div>
            <h1>gab_che terminal</h1>
        </div>

        <div class="right_header d-flex align-items-center">
            <button v-for="icon in iconList"><i class="fa-solid" :class=icon></i></button>
        </div>
    </div>
</template>

<style scoped lang="scss">
    @use '../styles/general.scss' as *;
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/utilities' as *;

    .top_header{
        background-color: $header_bg;
        color: $color_secondary;
        padding: $spacer_xs;
        cursor: move;
        @include flex_between;
    }

    .right_header,
    .left_header{
        gap: $spacer_xs;
    }

    .folder_icon,
    button{
        width: $icon_width;
        @include flex_center;
    }

    button{
        height: $icon_width;
        padding: $spacer_md;
    }

    h1{
        font-weight: 600;
        font-size: 15px;
        margin-bottom: 0;
    }
</style>