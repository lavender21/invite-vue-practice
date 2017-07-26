<template>
    <div class="contact-box">
        <div class="avatar"><img :src="avatar" alt=""></div>
        <div class="info">
            <div class="name">{{ name }}</div>
            <div class="skill">{{ skill }}</div>
            <div class="contact"><span>{{ info }}</span>{{ address }}</div>
        </div>
        <div class="check-box">
            <input type="checkbox" class="checks" :id="id" v-model="isChecked" @click="$emit('check')">
            <label :for="id"></label>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'contact',
        props: ['name', 'skill', 'info', 'avatar', 'id', 'address'],
        data() {
            return {
                isChecked: false
            }
        }
    }
</script>

<style lang="scss">
    $name-color: #8BB85D;
    $skill-color: #CCCCCC;
    $contact-color: #5D5D5D;
    $check-color: #E1E1E1;

    @mixin round-box($radius) {
        -webkit-border-radius: $radius;
        -moz-border-radius: $radius;
        border-radius: $radius;
        width: $radius;
        height: $radius;
    }

    .contact-box {
        display: flex;
        height: 6.2em;
        .avatar {
            img {
                @include round-box(4.7em);
            }
        }
        .info {
            margin-left: 1.5em;
            margin-top: 1em;
            width: 75%;
            .name {
                color: $name-color;
            }
            .skill {
                color: $skill-color;
                font-size: 0.7em;
            }
            .contact-box {
                font-size: 0.8em;
                span {
                    color: $contact-color;
                }
            }
        }
    }

    .check-box {
        display: flex;
        flex-direction: column;
        justify-content: center;
        .checks {
            visibility: hidden;
        }
        .checks + label {
            @include round-box(18px);
            border: 1px solid $check-color;
            margin-top: -2em;
        }
        .checks:checked + label {
            @include round-box(19px);
            background: url(../assets/basketball.png) no-repeat;
            background-size: 19px 19px;
        }
    }
</style>