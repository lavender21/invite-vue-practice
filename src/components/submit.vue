<template>
    <input type="submit" class="submit" :class="{disabled:isDisabled}" :disabled="isDisabled" value="invite" @click="onSubmit">
</template>

<script>
    export default{
        name: 'submit',
        data() {
            return {
                isDisabled:true,
                invited:[]
            }
        },
        methods:{
            onSubmit() {
                alert(this.invited + ' has been invited');
            }
        }
    }
</script>

<style lang="scss">
    $main-color: #E84F89;
    @mixin border-radius($radius){
        -webkit-border-radius:$radius;
        -moz-border-radius:$radius;
        border-radius:$radius;
    }
    .submit {
        width: 100%;
        height: 3.4em;
        font-size: 1em;
        text-transform: uppercase;
        color: #fff;
        border: 0;
        @include border-radius(4px);
        background: $main-color;
        margin-top: 1.7em;
    }

    input.disabled {
        cursor: not-allowed;
        background: #ccc;
    }

    input {
        outline: none;
    }
</style>