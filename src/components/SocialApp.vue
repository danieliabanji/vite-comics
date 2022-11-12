<template>
    <section class="bg-social">
        <div class="container social"> 
            <button type="button">sign-up now!</button>
            <div>
                <ul>
                    <a href="">Follow us</a>
                    <li v-for="(item, index) in social" :key="index">
                        <a :href="item.url" :class="{ 'active': item.current }">
                        <img :src="getImagePath(`../assets/img/${item.imageName}`)" :alt="item.text">
                        </a>
                    </li>
                </ul>
            </div>
        </div>

    </section>
</template>

<script>
import { socials } from '../data/dc-comics';

    export default {
        name: 'SocialApp',
        data(){
            return{
                social: socials,
            
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

.bg-social{ 
    justify-content: space-between;
    background-color: $darkgray;
    padding: 0.75rem;
    
}
button{
    text-transform: uppercase;
    background-color: $darkgray;
    color: $textwhite;
    border: 1px solid $blue;
    padding: 1rem;
    font-size: 1rem;
    cursor: pointer;

    &:hover{
        color: $black;
        background-color: $textwhite;
    }

}
.social{
    display: flex;
    justify-content: space-between;
    align-items: center;


    ul{
        list-style: none;
        padding: 1rem;
        @include dflex;
        align-items: unset;
        a{
            text-decoration: none;
            font-size: 1.75rem;
            color: $blue;
            &.active,
            &:hover{
                color: $textwhite;
            }
        }
        li {
            padding: 0 1rem;
        }
    }
}


</style>