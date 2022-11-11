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
        <div class="browserContainer">
            <div v-for="(item, index) in browserSection" :key="index" class="browser">
                <div>
                    <img :src="item.browserImg" alt="">
                </div>
                <span>{{ item.browserName }}</span>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'BrowseSectionsComponent',
    data() {
        return {
            browserSection: [
                {
                    browserName: 'digital comics',
                    browserImg: '../src/assets/img/buy-comics-digital-comics.png'
                },
                {
                    browserName: 'dc merchandise',
                    browserImg: '../src/assets/img/buy-comics-merchandise.png'
                },
                {
                    browserName: 'subscriptions',
                    browserImg: '../src/assets/img/buy-comics-subscriptions.png'
                },
                {
                    browserName: 'comic shop locator',
                    browserImg: '../src/assets/img/buy-comics-shop-locator.png'
                },
                {
                    browserName: 'dc power visa',
                    browserImg: '../src/assets/img/buy-dc-power-visa.svg'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;



section {
    height: 120px;
    background-color: $bluetext;

    .browserContainer {
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 120px;
        padding: 0 25px;
        width: 80vw;
        margin: 0 auto;

        .browser {
            height: 50px;

            div {
                height: 100%;
                display: inline-block;
                vertical-align: middle;
                margin-right: 10px;

                img {
                    height: 50px;
                }
            }

            span {
                vertical-align: middle;
                text-transform: uppercase;
                font-size: 12px;
                color: white;
            }

        }
    }
}
</style>