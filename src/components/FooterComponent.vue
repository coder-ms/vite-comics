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
        <div class="footerSec1">
            <div class="sectionOne">
                <div class="links">
                    <div>
                        <ul>
                            <li>
                                <h4>{{ footerSectionOne[0].titleSectionOne }}</h4>
                            </li>
                            <li v-for="item in footerSectionOne[0].linkSectionOne">{{ item }}</li>
                        </ul>
                        <ul>
                            <li>
                                <h4>{{ footerSectionOne[1].titleSectionOne }}</h4>
                            </li>
                            <li v-for="item in footerSectionOne[1].linkSectionOne">{{ item }}</li>
                        </ul>
                    </div>
                    <div>
                        <ul>
                            <li>
                                <h4>{{ footerSectionOne[2].titleSectionOne }}</h4>
                            </li>
                            <li v-for="item in footerSectionOne[2].linkSectionOne">{{ item }}</li>
                        </ul>
                    </div>
                    <div>
                        <ul>
                            <li>
                                <h4>{{ footerSectionOne[3].titleSectionOne }}</h4>
                            </li>
                            <li v-for="item in footerSectionOne[3].linkSectionOne">{{ item }}</li>
                        </ul>
                    </div>
                </div>

                <div class="imgContainer">
                    <img src="../assets/img/dc-logo-bg.png" alt="DC bigLogo">
                </div>
            </div>
        </div>

        <div class="footerSec2">
            <div class="sectionTwo">
                <div>
                    <div class="shopBtn">shop now !</div>
                </div>

                <div class="socials">
                    <h4>follow us</h4>
                    <img src="../assets/img/footer-facebook.png" alt="Facebook Icon">
                    <img src="../assets/img/footer-twitter.png" alt="Twitter Icon">
                    <img src="../assets/img/footer-youtube.png" alt="YouTube Icon">
                    <img src="../assets/img/footer-pinterest.png" alt="Pinterest Icon">
                    <img src="../assets/img/footer-periscope.png" alt="Periscope Icon">
                </div>
            </div>
        </div>
    </footer>
</template>
  
<script>

export default {
    name: 'FooterComponent',
    data() {
        return {
            footerSectionOne: [
                {
                    titleSectionOne: 'dc comics',
                    linkSectionOne: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
                },
                {
                    titleSectionOne: 'shop',
                    linkSectionOne: ['Shop DC', 'Shop DC Collectibles']
                },
                {
                    titleSectionOne: 'dc',
                    linkSectionOne: ['Terms Of Use', 'Privacy policy (new)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                },
                {
                    titleSectionOne: 'sites',
                    linkSectionOne: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                }
            ]
        }
    }
}
</script>
  
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

footer {


    .footerSec1 {
        height: 300px;
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;


        .sectionOne {
            display: flex;
            justify-content: space-between;
            height: 100%;
            position: relative;
            overflow: hidden;
            width: 80vw;
            margin: 0 auto;

            .links {
                display: flex;

                ul {
                    list-style: none;
                    color: grey;
                    font-size: 12px;
                    margin-right: 20px;

                    h4 {
                        font-size: 12px;
                        color: white;
                        text-transform: uppercase;
                        margin: 12px 0;
                    }

                    li {
                        padding: 2px 0;
                    }
                }
            }


            .imgContainer {
                display: flex;
                justify-content: flex-end;
                align-items: center;

                img {
                    width: 100%;
                }
            }
        }
    }

    .footerSec2 {
        height: 80px;
        width: 100%;
        background-color: rgb(49, 46, 46);

        .sectionTwo {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;
            width: 80vw;
            margin: 0 auto;

            div {
                .shopBtn {
                    border: 2px solid $bluetext;
                    padding: 5px 10px;
                    text-transform: uppercase;
                    color: white;
                    font-size: 12px;
                }
            }


            .socials {
                display: flex;
                justify-content: center;
                align-items: center;
                width: 40%;


                h4 {
                    color: $bluetext;
                    text-transform: uppercase;
                    font-weight: bolder;
                }

                img {
                    margin: 0 10px;
                }
            }
        }
    }


}
</style>
<!--
    COMANDO NPM per TERMINAL  li trovo su node module
    npm install bootstrap axios  @fortawesome/fontawesome-free
-->