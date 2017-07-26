<template>
    <header>
        <h1 class="title">Invite people to Dribbble</h1>
        <h2 class="subtitle"><span>{{count}}</span>invites available</h2>
        <search-box></search-box>
    </header>
</template>

<script>
    import searchBox from './searchBox.vue'

    export default {
        name: 'titleView',
        components:{ searchBox },
        data () {
            return {
                count: 0
            }
        }
    }
</script>

<style lang="scss">
    $subtitle-color:#999999;
    .center{
        text-align: center;
        vertical-align: center;
    }

    h1.title {
        @extend .center;
        font-size: 1.5em;
        height: 2.6em;
        line-height: 2.9em;
        letter-spacing: 2px;
    }

    h2.subtitle {
        @extend .center;
        font-size: 0.8em;
        color: $subtitle-color;
        line-height: 1em;
        letter-spacing: 1px;
    }
</style>