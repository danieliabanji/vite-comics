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
    export default {
        name: 'ShopComponent',
        data(){
            return{
                links:[
                    {
                        imageName: "buy-comics-digital-comics.png",
                        text:"Digital Comics",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "buy-comics-merchandise.png",
                        text:"DC Merchandise",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "buy-comics-subscriptions.png",
                        text:"Subscrition",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "buy-comics-shop-locator.png",
                        text:"Comic Shop Locator",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "buy-dc-power-visa.svg",
                        text:"DC Power Visa",
                        url: "#",
                        current: false,
                    },
                    
                ]
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