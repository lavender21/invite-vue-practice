<template>
    <div id="app" class="box">
        <titleView></titleView>
    </div>
</template>

<script>

import titleView from './titleView.vue'

export default {
    name: 'app',
    components: { titleView },
    data () {
        return {}
    }
}
</script>

<style lang="scss">
    $bg-color:rgba(0,0,0,0.75);
    $box-bg-color:#fff;
    $main-font-family: 'Arial';

    @mixin border-radius($radius){
        -webkit-border-radius:$radius;
        -moz-border-radius:$radius;
        border-radius:$radius;
    }

    html, body, div,h1,h2 {
        margin: 0;
        padding: 0;
    }

    html {
        height: 100%;
    }

    body {
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        background: $bg-color;
        font-family: $main-font-family;
    }

    .box {
        width: 28em;
        height: 36.8em;
        padding: 1.9em 2.9em;
        background: $box-bg-color;
        @include border-radius(4px);
    }
</style>
