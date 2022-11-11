<template>
   <div class="col">
        <a href="#"><img :src="obj.thumb" :alt="obj.sereis"></a>
        <p>{{ obj.series }}</p>
    </div>
</template>

<script>
    export default {
        name: 'ComicsComponent',
        props: [
        'obj'
    ]
    }
</script>

<style lang="scss" scoped>

</style>