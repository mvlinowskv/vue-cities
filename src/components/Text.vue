<template>
    <section class="text-center mx-auto background-grey py-4 py-lg-5 mx-0 mt-12" v-for="(background, index) in backgrounds" v-bind:key="background" v-bind:index="index">
        <div v-if="index%2==0" class="row mx-0">
                <div class="col-lg-8 order-2 order-lg-1 background-fixed background-cover background-center" v-bind:style="{'background-image': 'url(' + background.url + ')'}">
                <img :src="background.img" class="small-img float-end me-5 mt-5 mt-lg-0">
            </div>

            <div class="col-lg-4 order-1 order-lg-2">
                <div class="border-dark border-1 p-4">
                    <h3 class="font-15-2 color-black border-black border-h-left border-h-right text-uppercase w-max-content px-2 px-lg-3 mb-3 img-fluid mx-auto">
                        {{background.h3}}
                    </h3>
                    <p class="font-065-05 ml-auto">
                        {{background.text}}
                    </p>
                </div>
            </div>
            </div>
            
        <div v-else class="row mx-0">
            <div class="col-lg-4 order-1 order-lg-1">
                <div class="border-dark border-1 p-4">
                    <h3 class="font-15-2 color-black border-black border-h-left border-h-right text-uppercase text-center w-max-content px-2 px-lg-3 mb-3 mx-auto img-fluid">
                        {{background.h3}}
                    </h3>
                    <p class="font-065-05 ml-auto">
                        {{background.text}}
                    </p>
                </div>
            </div>

            <div class="col-lg-8 order-2 order-lg-2 background-fixed background-cover background-center" v-bind:style="{'background-image': 'url(' + background.url + ')'}">
                <img :src="background.img" class="small-img float-start ms-5 mt-5 mt-lg-0">
            </div>

            
        </div>
        
        
        
        
    </section>
</template>

<script>
import back1 from './img/adrien-olichon-QRtym77B6xk-unsplash.jpg'
import img1 from './img/robin-ooode-4ZtYoQavCVI-unsplash.jpg'

import back2 from './img/michele-bitetto-2y6ojwauKJI-unsplash.jpg'
import img2 from './img/marialaura-gionfriddo-oH88ODPLc40-unsplash.jpg'

import back3 from './img/pedro-lastra-suRvdiwP9Pk-unsplash.jpg'
import img3 from './img/mirko-bellabarba-HN-5Z6AmxrM-unsplash.jpg'

export default {
    name: 'Text',
    data() {
        return {
            backgrounds: [
                {   
                    url: back1,
                    img: img1,
                    h3: "Amsterdam Orientation", 
                    text: "The Amsterdam that most visitors experience is the city centre, the semi-circle with Central Station at its apex. It corresponds to the city as it was around 1850. Six major concentric canals ring the Old Centre; the Singel, the Herengracht, the Keizersgracht, the Prinsengracht, the Lijnbaansgracht, and the Singelgracht, together forming the Canal Ring. Other districts inside the city centre are the Jordaan, a former working-class area gone upmarket, and Plantage."
                },
                {
                    url: back2,
                    img: img2,
                    h3: "Roma Orientation",
                    text: "Situated on the river Tiber, between the Apennine mountains and the Tyrrhenian Sea, the Eternal City was once the administrative centre of the mighty Roman Empire, ruling over a vast territory that stretched all the way from Britain to Mesopotamia. Today, the city is the seat of the Italian government and home to numerous ministerial offices. Rome has 2.6 million inhabitants while its metropolitan area is home to around 4.2 million."
                },
                {
                    url: back3,
                    img: img3,
                    h3: "Paris Orientation",
                    text: "The city of Paris itself is officially divided into 20 districts called arrondissements, numbered from 1 to 20 in a clockwise spiral from the centre of the city (which is known as Kilometre Zero and is located at the front of Notre Dame). Arrondissements are named according to their number. You might, for example, stay in the 5th, which would be written as 5e in French."
                }
            ]
            
        }
    }
}
</script>
