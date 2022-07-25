<template>
  <Slider/>
  <TextImage h1_text="Beautiful places" 
  description='Situated on the river Tiber, between the Apennine mountains and the Tyrrhenian Sea, the "Eternal City" was once the administrative centre of the mighty Roman Empire, ruling over a vast territory that stretched all the way from Britain to Mesopotamia. Today, the city is the seat of the Italian government and home to numerous ministerial offices. Rome has 2.6 million inhabitants while its metropolitan area is home to around 4.2 million.
Architecturally and culturally, Rome has some contrasts - you have areas with pompously huge majestic palaces, avenues and basilicas which are then surrounded by tiny alleyways, little churches and old houses; you may also find yourself walking from a grand palace and tree-lined elegant boulevard, into a small and cramped Medieval-like street.
'></TextImage>


<HoverCards></HoverCards>

<!-- <img src="./components/img/piotr-chrobot-M4EcjtmE01k-unsplash.jpg"> -->
<Text></Text>


</template>

<script>
import Slider from './components/Slider.vue'
import TextImage from './components/TextImage.vue'
import HoverCards from './components/HoverCards.vue'
// import BackgroundFixed from './components/BackgroundFixed.vue'
import Text from './components/Text.vue'

export default {
  name: 'App',
  components: {
    Slider,
    TextImage,
    HoverCards,
    // BackgroundFixed,
    Text
  }
}

</script>

<style>

</style>
