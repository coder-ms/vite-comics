<template>
  <HeaderComponent />

  <main>
    <ProductList />
  </main>

  <FooterComponent />
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ProductList from './components/ProductList.vue';

export default {
  components: {
    HeaderComponent,
    ProductList,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>

</style>

