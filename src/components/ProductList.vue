<!--
Esercizio di oggi: Vite DC Comics
nome repo: vite-comics
Descrizione:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!

Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

Esercizio di oggi: *Vite DC Comics*
nome repo: vite-comics
*Descrizione:*
Continuate a lavorare nella stessa repo di ieri e create un nuovo componente per visualizzare le card dei fumetti, prendendo i dati dal file json che trovate in allegato e un nuovo componente per il jumbotron.
Una volta inseriti tutti i contenuti dinamicamente, completate il vostro layout e rifinite i dettagli con Sass.

Bonus
Definire propri array per tutti i menu e generare dinamicamente le varie navbar
-->

<template>
    <section>
        <!--JUMBOTRON TEEN TITANS GO-->
        <div class="jumbotron">

        </div>
        <!--GALLERIA COMICS-->
        <div class="gallery">
            <div class="widthGallery">

                <!--TITOLO: CUURENT SERIES USARE TRANSFORM TRANSLATE-->
                <div class="currentSeries">
                    <h4>CURRENT SERIES</h4>
                </div>
                <!--GALLERIA IMMAGINI: 12 IMMAGIN, 6 PER RIGA USARE FLEX-WRAP: WRAP-->
                <div class="galleryImages">

                    <div class="structGallery" v-for="(comic, index) in arrayComics" :key="index">
                        <div class="imgGalleryContainer">
                            <img :src="comic.thumb" :alt="comic.series">
                        </div>
                        <div class="infoDC">
                            <span>{{ comic.series }}</span>
                        </div>
                    </div>
                </div>
                <!--GALLERY BUTTON-->
                <div class="galleryButton">
                    LOAD MORE
                </div>
            </div>
        </div>



    </section>
</template>
  
<script>
import { infoComics } from '../comicData/arrays.js';

export default {
    name: 'ProductList',
    data() {
        return {
            arrayComics: infoComics,
        }
    }
}
</script>
  
<style lang="scss" scoped>
@use '../assets/styles/partials/variables' as *;
@use '../assets/styles/partials/mixins' as *;

section {
    width: 100%;

    .jumbotron {
        height: 380px;
        background: url('../assets/img/jumbotron.jpg');
    }

    .gallery {
        height: 560px;
        background-color: rgb(36, 33, 33);

        .widthGallery {
            width: 70%;
            margin: 0 auto;

            .currentSeries {
                text-align: center;
                display: flex;
                transform: translate(-2rem, -1.5ex);
                width: 180px;
                height: 35px;
                align-items: center;
                justify-content: center;
                border: 1px solid $bluetext;
                background-color: $bluetext;
                color: white;
                font-size: 16px;
                font-weight: 600;
            }

            .galleryImages {
                height: 450px;
                //border: 1px solid red;
                display: flex;
                flex-wrap: wrap;
                padding: 10px;

                .structGallery {
                    width: calc(100% / 6);
                    height: calc(100% / 2);
                    //border: 1px solid white;
                    padding: 0 10px;

                    .imgGalleryContainer {
                        height: 75%;
                        width: 100%;
                        background-color: blue;
                        //border: 1px solid white;

                        img {
                            height: 100%;
                            width: 100%;
                        }
                    }

                    .infoDC {
                        margin-top: 5px;
                        padding: 3px 0;
                        height: 20%;
                        width: 100%;
                        //background-color: green;
                        //border: 1px solid white;


                        span {
                            color: white;
                            font-size: 12px;
                            text-transform: uppercase;
                            text-align: start;
                        }
                    }
                }
            }
        }

        .galleryButton {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 120px;
            height: 35px;
            margin: 0 auto;
            border: 1px solid $bluetext;
            background-color: $bluetext;
            color: white;
            font-size: 14px;
            font-weight: 600;
            margin-top: 20px;
        }
    }
}
</style>