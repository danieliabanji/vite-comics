<template>
  <HeaderComponent/>
  <main>
    <JumboComponent/>
    <ComicsList/>
    <ShopComponent/>
  </main>
  <FooterComponent/>
  
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import ComicsList from './components/ComicsList.vue';
import ShopComponent from './components/ShopComponent.vue';
import FooterComponent from './components/FooterComponent.vue';

  export default {
  components: {
    HeaderComponent,
    JumboComponent,
    ShopComponent,
    FooterComponent,
    ComicsList
}
}
</script>

<style lang="scss" scoped>

</style>