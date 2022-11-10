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
    <header>
        <a href="#">
            <img src="../assets/img/dc-logo.png" alt="DC Logo">
        </a>
        <nav>
            <ul>
                <li v-for="(link, index) in links" :key="index">
                    <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>
  
<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            links: [

            ]
        }
    }
}
</script>
  
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

header {
    text-align: center;

    ul {
        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include dflex;

        li a {
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s;
            color: $blacktest;

            &.active,
            &:hover {
                //lighten(, 70%)
                background: $lightblue;
            }
        }
    }
}
</style>
  