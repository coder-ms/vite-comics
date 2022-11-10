<!--
Esercizio di oggi: Vite DC Comics
nome repo: vite-comics
Descrizione:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!

Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.
-->
<template>
    <section>
        Sono section prodotti
    </section>
</template>
  
<script>
export default {
    name: 'ProductList'
}
</script>
  
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;


section {
    text-align: center;
    margin: 3rem 0;
}
</style>