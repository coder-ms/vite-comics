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
        <!--JUMBVOTRON TEEN TITANS GO-->
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

                    <!--RIPETERE STRUTTURA UNA SOLA VOLTA(MEDIA QUERY) -->

                    <!--
                    <div class="col">
                        <img :src="obj.src" :alt="obj.titolo">
                        <h4>{{ obj.titolo }}</h4>
                    </div>
                    -->

                    <!--ESEMPIO BASE, NON DINAMICO (DA CANCELLARE)-->
                    <div class="structGallery">
                        <div class="imgGalleryContainer">
                            <img src="https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX"
                                alt="">
                        </div>
                        <div class="infoDC">
                            <span>Batman: White Knight Presents: Harley Quinn</span>
                        </div>
                    </div>

                </div>
            </div>
            <!--GALLERY BUTTON-->
            <div class="galleryButton">
                LOAD MORE
            </div>

        </div>
    </section>
</template>
  
<script>
export default {
    name: 'ProductList',
    infoComics: [
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
            "price": "$19.99",
            "series": "Action Comics",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
            "price": "$3.99",
            "series": "American Vampire 1976",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
            "price": "$16.99",
            "series": "Aquaman",
            "type": "graphic novel"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
            "price": "$2.99",
            "series": "Batgirl",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            "price": "$3.99",
            "series": "Batman",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
            "price": "$2.99",
            "series": "Batman Beyond",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
            "price": "$3.99",
            "series": "Batman/Superman",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
            "price": "$4.99",
            "series": "Batman/Superman Annual",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
            "price": "$5.99",
            "series": "Batman: The Joker War Zone",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
            "price": "$6.99",
            "series": "Batman: Three Jokers",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
            "price": "$4.99",
            "series": "Batman: White Knight Presents: Harley Quinn",
            "type": "comic book"
        },
        {
            "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
            "price": "$16.99",
            "series": "Catwoman",
            "type": "graphic novel"
        }
    ]
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
        height: 550px;
        background-color: rgb(36, 33, 33);

        .widthGallery {
            width: 80%;
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
                border: 1px solid red;
                padding: 0 10px;
                display: flex;
                flex-wrap: wrap;

                .structGallery {
                    width: calc(100% / 6);
                    height: calc(100% / 2);
                    border: 1px solid white;
                    padding: 0 10px;

                    .imgGalleryContainer {
                        height: 75%;
                        width: 100%;
                        background-color: blue;
                        border: 1px solid white;

                        img {
                            height: 165px;
                            width: 165px;
                        }
                    }

                    .infoDC {
                        margin-top: 5px;
                        height: 20%;
                        width: 100%;
                        background-color: green;
                        border: 1px solid white;
                        display: flex;
                        justify-content: center;
                        align-items: center;

                        span {
                            color: white;
                            font-size: 12px;
                            text-transform: uppercase;
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