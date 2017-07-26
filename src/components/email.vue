<template>
    <input type="email" class="email" placeholder="Send invite by e-mail">
</template>

<script>
    export default{
        name:'email',
        data() {
            return{}
        }
    }

</script>

<style lang="scss">
    $email-color:#E1E1E1;
    @mixin border-radius($radius){
        -webkit-border-radius:$radius;
        -moz-border-radius:$radius;
        border-radius:$radius;
    }

    .email {
        width: 99%;
        height: 3.3em;
        border: 1px solid $email-color;
        @include border-radius(4px);
        text-indent: 1em;
        font-size:0.8em;
    }

    .email::placeholder {
        color: $email-color;
    }
    input{
        outline: none;
    }
</style>