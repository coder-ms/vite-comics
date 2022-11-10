<template>
    <footer>
        <div class="col container">
            <a href="#">
                <img src="../assets/img/la-molisana-logo.png" alt="La Molisana">
            </a>
        </div>
        <div class="footer-links">
            <h4>Pastificio</h4>
            <nav>
                <!--
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                    </li>
                </ul>
                -->
                <ul>
                    <li><a href="#">Il Pastificio</a></li>
                    <li><a href="#">Il grano</a></li>
                    <li><a href="#">Filiera</a></li>
                    <li><a href="#">100 anni di pasta</a></li>
                    <li><a href="#">Sartoria della pasta</a></li>
                </ul>
            </nav>
        </div>
        <div class="footer-links">
            <h4>prodotti</h4>
            <nav>
                <ul>
                    <li><a href="#">Le Classiche</a></li>
                    <li><a href="#">Le Intengrali</a></li>
                    <li><a href="#">Le Speciali</a></li>
                    <li><a href="#">Le Biologiche</a></li>
                    <li><a href="#">Le Gluten-free</a></li>
                </ul>
            </nav>
        </div>

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