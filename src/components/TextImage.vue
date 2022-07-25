<template>
    <div class="w-100 text-center py-3 container-fluid">
        <h2 class="font-15-2 color-black border-black border-h-left border-h-right text-uppercase w-max-content mx-auto px-2 px-lg-3">
            {{h1_text}}
        </h2>

        <div class="d-flex align-items-center justify-content-center row">
            <div class="font-065-05 text-center text-md-center col-12 col-md-6 order-2 order-md-1 ps-lg-4">
                <p class="font-family-zilla text-left px-4 mt-4 mt-md-0">{{description}}</p>
            </div>
            <div class="col-12 col-md-6 order-1 order-md-2">
                <img :src="imageRight" class="h-circle-img w-circle-img object-fit-cover object-position-right rounded-circle "/>
            </div>
            
        </div>
    </div>
</template>

<script>

import BackgroundImageAmsterdam from './img/thais-cordeiro-sKwoOmuSqMs-unsplash.jpg'
import ImageColumn from './img/carlos-ibanez-oI141-aIwnQ-unsplash-1920.jpg'
    export default {
        name: 'TextImage',
        props: {
            h1_text: String,
            description: String
        },
        data() {
            return {
                background: BackgroundImageAmsterdam,
                imageRight: ImageColumn
            }
        }
        
    }
</script>