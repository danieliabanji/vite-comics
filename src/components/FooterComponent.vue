<template>
    <footer>
        <div class="logo"> 
            <div class="cols container">
                <FooterMenu v-for="(menu,index) in navBars" :key="index" :item="menu"/>
    
            </div>
    
        </div>
        <SocialApp/>
    </footer>
</template>

<script>
import {menu} from '../data/dc-comics'
import FooterMenu from './FooterMenu.vue'
import SocialApp from './SocialApp.vue'
    export default {
        components:{
            SocialApp,
            FooterMenu
        },
        name: 'FooterComponent',
        data(){
            return{
                navBars: menu,
                
            }
        }
    }
</script>

<style lang="scss">
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

footer{
    background-image: url("../assets/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    // padding: 3rem;

    


    
    .cols{
        
        display: flex;
        padding: 3rem 0;
        .footer-links{
            
            flex-basis: calc(100% / 7);
            padding: 0 1rem;
        }

        h4{
            text-transform: uppercase;
            font-size: 1.25rem;
            font-weight: 600;
            margin: 1rem 0;
            color: $textwhite;
        }

        ul{
            list-style: none;
            padding: unset;

            li a{
                display: inline-block;
                margin-bottom: 0.25rem;
                text-decoration: none;
                font-size: 0.875rem;
                // padding: 1rem;
                color: $textgray;


                &.active,
                &:hover{
                color: $blue;
            }
            }
        }
    }
}
.logo{
        background-image: url("../assets/img/dc-logo-bg.png");
        background-repeat: no-repeat;
        background-position: 1000px;
    }

</style>