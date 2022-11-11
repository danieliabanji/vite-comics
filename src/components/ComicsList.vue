<template>
    <section class="products">
        <div id="current" class="btn btn-primary text-white text-uppercase ">current series</div>
        <div class="container">
            <div class="row">
                <ComicsComponent v-for="(item, index) in comic" :key="index" :obj="item"/>
            </div>
            <button class="btn btn-primary text-uppercase ">load more</button>
        </div>
    </section>
</template>

<script>
import {comics} from '../data/dc-comics.js'
import ComicsComponent from './ComicsComponent.vue';
    export default {
    name: "ComicsList",
    components: { 
        ComicsComponent
    },
    data() {
        return {
            comic: comics, 
        }
    },
   
}
</script>

<style lang="scss" >
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


#current{
    align-items: flex-end;
    margin-right: 1150px;
    margin-top: -20px;
    font-weight: 600;
    border-radius: 0%;
}
.products {
    padding: 0rem 1rem;
    text-align: center;
    background-color: $black;

    .row {
        flex-flow: wrap;
        .col {
            flex-basis: calc(100% / 6);
            padding: 1rem;

            img{
                width: 200px;
                height: 200px;
                object-fit: cover ;
                object-position: 50% 0%;
            }

            p{
                text-transform: uppercase;
                font-size: 0.95rem;
                margin-top: 1rem;
                text-align: start;
                color: $textwhite;
            }
        }
    }
    button{
        color: $textwhite;
        border-radius: 0%;
        width: 200px;
        margin-bottom: 1rem;
    }

}

</style>