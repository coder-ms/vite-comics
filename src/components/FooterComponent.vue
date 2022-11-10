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
    <footer>


    </footer>
</template>
  
<script>
export default {
    name: 'FooterComponent'
}
</script>
  
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

footer {
    text-align: center;
    margin-bottom: 3rem;
    display: flex;

    .logo,
    .footer-links {
        flex-basis: calc(100% / 3);
        padding: 0 1rem;
    }

    h4 {
        text-transform: uppercase;
        font-size: 1.25rem;
        font-weight: 600;
    }

    ul {
        list-style-type: none;

        li a {
            display: inline-block;
            text-decoration: none;
            margin-bottom: 0.25rem;
            font-size: 0.875rem;
            color: $bluetext;


            &:hover {
                //lighten(, 70%)
                background: $primary;
            }
        }
    }
}
</style>
<!--
    COMANDO NPM per TERMINAL  li trovo su node module
    npm install bootstrap axios  @fortawesome/fontawesome-free
-->