<template>
  <HeaderComponent/>
  <main>
    <JumboComponent/>
    <ShopComponent/>
  </main>
  <FooterComponent/>
  
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import ShopComponent from './components/ShopComponent.vue';

  export default {
  components: {
    HeaderComponent,
    JumboComponent,
    ShopComponent,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>

</style>