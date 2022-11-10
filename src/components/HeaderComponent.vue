<template>
    <header>
        <a href="#">
            <img src="../assets/img/la-molisana-logo.png" alt="La Molisana">
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
                {
                    text: "Home",
                    url: "#",
                    current: false,
                },
                {
                    text: "Prodotti",
                    url: "#",
                    current: true,
                },
                {
                    text: "Chi Siamo",
                    url: "#",
                    current: false,
                },
                {
                    text: "Contatti",
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
  