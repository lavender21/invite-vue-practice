<template>
    <div class="search-box">
        <input type="text" id="search" class="search" />
        <icon name="search" class="icon"></icon>
    </div>
</template>

<script>

    export default {
        name: 'search-box',
        data () {
            return {
                isActive: false
            }
        }
    }
</script>

<style lang="scss">
    $input-color: #EBEBEB;
    .search-box {
        position: relative;
        height: 5em;
        .search {
            width: 92%;
            height: 2em;
            border: 0;
            border-bottom: 1px solid $input-color;
            margin-top: 2.1em;
            transition: .5s ease;
        }
        .search:focus {
            width: 100%;
            border: 1px solid $input-color;
            margin-top: 3em;
        }
        .icon {
            position: absolute;
            right: 0;
            top: 2em;
            font-size: 1.2em;
            color: $input-color;
        }
    }

    input {
        outline: none;
    }
</style>