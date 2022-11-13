<template>
    <div class="footer-links">
        <h4>{{ item.title }}</h4>
        <nav>
            <ul>
                <li v-for="(link, index) in item.links" :key="index"><a :href="link.url">{{ link.text }}</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
    export default {
        name: 'FooterMenu',
        props:[
            'item'
        ]
    }
</script>

<style lang="scss" scoped>

</style>