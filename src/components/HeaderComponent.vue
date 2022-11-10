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
                    <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}
                    </a>
                </li>
                <!--CAPIRE COME METTERE -->
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
                {
                    text: "Characters",
                    url: "#",
                    current: false,
                },
                {
                    text: "Comics",
                    url: "#",
                    current: true,
                },
                {
                    text: "Movies",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "Games",
                    url: "#",
                    current: false,
                },
                {
                    text: "Collectibles",
                    url: "#",
                    current: false,
                },
                {
                    text: "Videos",
                    url: "#",
                    current: false,
                },
                {
                    text: "Fans",
                    url: "#",
                    current: false,
                },
                {
                    text: "News",
                    url: "#",
                    current: false,
                },
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
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
    display: flex;
    justify-content: space-around;
    align-items: center;

    a {
        display: flex;
        justify-content: flex-start;
        align-items: center;

        img {
            width: 100%;
        }
    }

    nav {
        text-align: center;
        display: flex;
        justify-content: flex-start;

        ul {
            list-style: none;
            margin: 2.5rem 1rem;
            @include dflex;

            li {
                a {
                    text-transform: uppercase;
                    display: inline-block;
                    padding: 3rem 0.75rem;
                    text-decoration: none;
                    font-weight: 600;
                    margin: 0 0.5rem;
                    font-size: 0.75rem;
                    transition: background 0.3s;

                    &.active,
                    &:hover {
                        color: $bluetext;
                        border-bottom: 6px solid $bluetext;
                    }
                }
            }
        }
    }
}
</style>
  