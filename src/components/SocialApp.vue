<template>
    <section class="bg-social">
        <div class="container social"> 
            <button type="button">sign-up now!</button>
            <div>
                <ul>
                    <a href="">Follow us</a>
                    <li v-for="(social, index) in socials" :key="index">
                        <a :href="social.url" :class="{ 'active': social.current }">
                        <img :src="getImagePath(`../assets/img/${social.imageName}`)" :alt="social.text">
                        </a>
                    </li>
                </ul>
            </div>
        </div>

    </section>
</template>

<script>
    export default {
        name: 'SocialApp',
        data(){
            return{
                socials:[
                    {
                        imageName: "footer-facebook.png",
                        text:"facebook",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "footer-twitter.png",
                        text:"twitter",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "footer-youtube.png",
                        text:"youtube",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "footer-pinterest.png",
                        text:"pinterest",
                        url: "#",
                        current: false,
                    },
                    {
                        imageName: "footer-periscope.png",
                        text:"periscope",
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