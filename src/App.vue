<template>
  <HeaderComponent />

  <main>
    <ProductList />
  </main>
  <SectionBrowserComponent />
  <FooterComponent />
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import SectionBrowserComponent from './components/SectionBrowserComponent.vue';
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

