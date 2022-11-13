<template>
  <HeaderComponent />
  <ProductList />

  <MainComponent />
  <FooterComponent />
</template>

<script>

import HeaderComponent from './components/HeaderComponent.vue';
import ProductList from './components/ProductList.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';



export default {
  components: {
    HeaderComponent,
    ProductList,
    MainComponent,
    FooterComponent
  }
}
</script>

<style lang="scss" scoped>

</style>


<!--
<template>
  <HeaderComponent/>
  <CurrentSeriesComponent/>
  <BrowseSectionsComponent/>
  <FooterComponent/>
</template>

<script>
  import HeaderComponent from './components/HeaderComponent.vue';
  import FooterComponent from './components/FooterComponent.vue';
  import BrowseSectionsComponent from './components/BrowseSectionsComponent.vue';
  import CurrentSeriesComponent from './components/CurrentSeriesComponent.vue';
  export default {
    components: {
      HeaderComponent,
      FooterComponent,
      BrowseSectionsComponent,
      CurrentSeriesComponent
    }
  }
</script>
-->

