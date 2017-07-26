<template>
    <div id="app" class="box">
        <titleView></titleView>
        <contact v-for="contact in contacts" :key="contact.id" :name="contact.name" :skill="contact.skill" :info="contact.info"
        :address="contact.address" :id="contact.id" :avatar="contact.avatar"></contact>
        <email></email>
    </div>
</template>

<script>

import titleView from './components/titleView.vue'
import contact from './components/contact.vue'
import email from './components/email.vue'

export default {
    name: 'app',
    components: { titleView, contact,email},
    data () {
        return {
            contacts:[
                {
                    name: 'Alex',
                    skill: 'photoshop,pinanacle studio',
                    info: 'Belarus',
                    address: 'bymart.by',
                    id: 0,
                    avatar: 'http://i.pravatar.cc/100?img=3'
                },
                {
                    name: 'Alina',
                    skill: '',
                    info: 'Ukraine Kiev',
                    address: 'Kuvshynonva.com',
                    id: 1,
                    avatar: 'http://i.pravatar.cc/100?img=4'
                },
                {
                    name: 'Yolna',
                    skill: 'wordpress,web design,joomla,html',
                    info: 'palama de Mallorica',
                    address: 'yollandagranados.com',
                    id: 2,
                    avatar: 'http://i.pravatar.cc/100?img=5'
                }
            ]
        }
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
