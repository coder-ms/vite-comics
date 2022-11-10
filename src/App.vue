<template>
  <HeaderComponent />

  <main>
    <ProductList />
    <SectionBrowserComponent />
  </main>

  <FooterComponent />
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import SectionComponent from './components/SectionBrowserComponent.vue';
import ProductList from './components/ProductList.vue';

export default {
  components: {
    HeaderComponent,
    ProductList,
    SectionBrowserComponent,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>

</style>

