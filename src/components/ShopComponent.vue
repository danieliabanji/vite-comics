<template>
    <section>
    <div class="container">
        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url" :class="{ 'active': link.current }">
                    <img :src="getImagePath(`../assets/img/${link.imageName}`)" :alt="link.text">
                    {{ link.text }}
                    </a>
                </li>
            </ul>
        </nav>
    </div>

    </section>
</template>

<script>
import { shop } from '../data/dc-comics';

    export default {
        name: 'ShopComponent',
        data(){
            return{
                links : shop
               
            }

        },
        methods: {
            getImagePath: function(imgPath){
                return new URL(imgPath, import.meta.url).href;
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section{
    background-color: $blue;

    nav{

        ul{
        list-style: none;
        padding: 2.5rem;
        margin-bottom: unset;
        @include dflex;

        li a{
            @include dflex;
            padding: 1rem;
            text-decoration: none;
            color: $textwhite;
            &.active,
            &:hover{
                color: $black;
            }
            img{
                height: 60px;
                margin-right: 1rem;
            }
            
        }
    }

    }
    
}


</style>