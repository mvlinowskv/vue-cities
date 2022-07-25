<template>
    <section class="row justify-content-center mx-0 my-5">
        <div  v-for="card in cards" v-bind:key="card" class="col-md-4 cursor-pointer px-0 overflow-hidden h-80vh background-cover background-center card-feature" v-bind:style="{'background-image': 'url(' + card.background + ')'}">
            
            <div class="card-text position-relative mx-auto">
                <div class="background-grey w-75 mx-auto p-3">
                    <h4 class="text-uppercase border-dark border-1 border-start border-end px-2 w-max-content mx-auto">{{card.title}}</h4>
                </div>
            <div class="py-3 px-4 mr-auto background-grey position-relative w-90 mx-auto">
                
                <div class="p-3 px-lg-5 text-center">
                    
                    <p class="font-family-zilla font-07-05">{{card.description}}</p>
                </div>
                
            </div>
            </div>
            
        </div>
    </section>

</template>
    
<script>

import BackgroundOne from './img/pexels-daria-shevtsova-3597067.jpg'
import BackgroundTwo from './img/alexandre-wavrant-U4K2Gzfbr5g-unsplash.jpg'
import BackgroundThree from './img/pexels-olenka-sergienko-3686798.jpg'

    export default {
        name: 'HoverCards',

        data() {
            return {
                cards: [
                    {
                        title: 'Paris',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                        background: BackgroundOne
                    },

                     {
                        title: 'Roma',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                        background: BackgroundTwo
                    },

                     {
                        title: 'Amsterdam',
                        description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
                        background: BackgroundThree
                    }
                ]
            }
        }
    }
</script>