<template>
    <section>
        <div class="container">
            <p>&RightArrow; Content goes here &leftarrow;</p>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'JumboComponent',
    }
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section{
    background-color: $black;

    div{
        padding: 4rem 1rem;
        position: relative; 
        width: 100%;
        display: flex;
        align-items: center;
        
        &:before{
            content: "";
            background-image: url("../assets/img/jumbotron.jpg");
            background-size: cover;
            position: absolute;
            top: 0px;
            right: 0px;
            bottom: 0px;
            left: 0px;
            opacity: 0.6;
        }
        p{
            position: relative;
            color: $textwhite;
            font-weight: 600;
            font-size: 2.5rem;
        }
        
    }
}

</style>