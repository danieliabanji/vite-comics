<template>
    <header class="container">
    <a href="">
        <img src="../assets/img/dc-logo.png" alt="DC Logo">
    </a>
    <nav>
        <ul>
            <li v-for="(link,index) in links" :key="index">
                <a :href="link.url" :class="{'active' : link.current}">{{link.text}}</a>
            </li>
        </ul>
    </nav>
    </header>
</template>

<script>
    export default {
        name: 'HeaderComponent',
        data(){
            return{
                links:[
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
                    {
                        text:"Shop",
                        url: "#",
                        current: false,
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

header{
    @include dflex;
    justify-content: space-between;

    ul{
        list-style: none;
        margin: 2.5rem 1rem 0rem;
        @include dflex;

        li a{
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            color: $black;
            font-weight: 600;
            padding-bottom: 50px;

            &.active,
            &:hover{
                color: $blue;
                border-bottom: 5px solid $blue;
            }
        }
    }
}

</style>