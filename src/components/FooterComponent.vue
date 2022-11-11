<template>
    <footer>
        <div class="logo"> 
            <div class="cols container">
    
                <div class="footer-links">
                    <h4>Dc Comics</h4>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in comics" :key="index">
                                <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                            </li>
                        </ul>
                    </nav>
                    <h4>Shop</h4>
                    <ul>
                        <li v-for="(link, index) in shop" :key="index">
                            <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                        </li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Dc</h4>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in dc" :key="index">
                                <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                            </li>
                        </ul>
                    </nav>
    
                </div>
                <div class="footer-links">
                    <h4>Sites</h4>
                    <nav>
                        <ul>
                            <li v-for="(link, index) in sites" :key="index">
                                <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                            </li>
                        </ul>
                    </nav>
    
                </div>
    
            </div>
    
        </div>
        <SocialApp/>
    </footer>
</template>

<script>
import SocialApp from './SocialApp.vue'
    export default {
        components:{
            SocialApp,
        },
        name: 'FooterComponent',
        data(){
            return{
                comics:[
                    {
                        text:"Characters",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Comics",
                        url: "#",
                        current: true,
                    },
                    {
                        text:"Movies",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Tv",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Games",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Collectibles",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Videos",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Fans",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"News",
                        url: "#",
                        current: false,
                    },
                    
                ],
                shop:[
                    {
                        text:"Shop DC",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Shop DC Collectibles",
                        url: "#",
                        current: false,
                    },
                ],
                dc:[
                    {
                        text:"Terms Of Use",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Pricacy policy (New)",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Ad Choices",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Advertising",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"jobs",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Subscriptions",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Talent Workshops",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"CPSC Certifivstes",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Rating",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Shop Help",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"Contact Us",
                        url: "#",
                        current: false,
                    },
                    

                ],
                sites:[
                    {
                        text:"DC",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"MAD Magazine",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"DC Kids",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"DC Univers",
                        url: "#",
                        current: false,
                    },
                    {
                        text:"DC Power Visa",
                        url: "#",
                        current: false,
                    },
                ],
            }
        }
    }
</script>

<style lang="scss" scoped>
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