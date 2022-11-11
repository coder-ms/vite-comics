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
        <div class="jumbotron">

        </div>
        <div class="gallery">
            <div class="widthGallery">
                <div class="currentSeries">
                    CURRENT SERIES
                </div>
                <div class="galleryImages">
                    <!--
                    <ul>
                        <li>
                            <img src="" alt="">
                            <p>CIAO</p>
                        </li>
                    </ul>
                    -->
                </div>
                <div class="galleryButton">
                    LOAD MORE
                </div>
            </div>


        </div>
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
    width: 100%;
    text-align: center;

    .jumbotron {
        height: 380px;
        background: url('../assets/img/jumbotron.jpg');
    }

    .gallery {
        height: 450px;
        background-color: rgb(36, 33, 33);

        .widthGallery {
            width: 80%;
            margin: 0 auto;

            .currentSeries {
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
                height: 350px;
                border: 1px solid red;
            }

            .galleryButton {
                display: flex;
                align-items: center;
                justify-content: center;
                width: 120px;
                height: 35px;
                border: 1px solid $bluetext;
                background-color: $bluetext;
                color: white;
                font-size: 14px;
                font-weight: 600;
                margin-top: 20px;
                transform: translate(450%);
            }
        }
    }
}
</style>