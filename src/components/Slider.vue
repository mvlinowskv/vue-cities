<template>
  <div id="slider-slider" class="wrapper" v-cloak v-bind:class="{'is-previous': isPreviousSlide, 'first-load': isFirstLoad}">
  <div class="slide-wrapper h-100vh background-fixed background-cover background-center" v-for="(slide, index) in slides" v-bind:class="{ active: index === currentSlide }" v-bind:style="{ 'z-index': (slides.length - index), 'background-image': 'url(' + slide.bgImg + ')' }"
       v-on:mouseover="stopRotation"
      v-on:mouseout="startRotation"
      v-bind:key="slide">
    <div class="slide-inner">
      <div class="slide-bg-text text-uppercase">
        <p>{{ slide.headlineFirstLine }}</p>
        <p>{{ slide.headlineSecondLine }}</p>
      </div>
      <div class="slide-rect-filter">
        <div class="slide-rect" v-bind:style="{'border-image-source': 'url(' + slide.rectImg + ')'}"></div>
      </div>
      <div class="slide-content">
        <h1 class="slide-content-text font-2-3 text-uppercase">
          <p>{{ slide.headlineFirstLine }}</p>
          <p>{{ slide.headlineSecondLine }}</p>
        </h1><a class="slide-content-cta">Call To Action</a></div>
      <h2 class="slide-side-text"><span>{{ slide.sublineFirstLine }} / </span><span>{{ slide.sublineSecondLine }}</span></h2>
    </div>
  </div>
  <div class="controls-container position-absolute d-flex align-items-end">
    <button class="controls-button outline-0 border-0" v-for="(slide, index) in slides" v-bind:class="{ active: index === currentSlide }" @click="updateSlide(index)"
      v-on:mouseout="startRotation" v-bind:key="slide">{{ slide.headlineFirstLine }} {{ slide.headlineSecondLine }}</button>
  </div>
  <div class="pagination-container">
    <span class="pagination-item outline-0 border-0" v-for="(slide, index) in slides" v-bind:class="{ active: index === currentSlide }" @click="updateSlide(index)"
            v-on:mouseout="startRotation" v-bind:key="slide"></span>
  </div>
</div>
</template>

<script>
  // All of your components JS code lives within this section
  // we can still do things such as `import lib from 'lib'` should we wis
  import ParisImage from './img/leonard-cotte-R5scocnOOdM-unsplash.jpg';
  import RomaImage from './img/michele-bitetto-1AQTOjczEB0-unsplash.jpg';
  import AmsterdamImage from './img/max-van-den-oetelaar--e4vLFZV9QM-unsplash.jpg';

  export default {
    name: "Slider",
    data() {
        return {
            currentSlide: 0,
            isPreviousSlide: false,
            isFirstLoad: true,
            slides: [
                        {
                            headlineFirstLine: "Beautiful",
                            headlineSecondLine: "Paris",
                            sublineFirstLine: "Bonjour",
                            sublineSecondLine: "bonne journée",
                            bgImg: ParisImage,
                            rectImg: ParisImage
                        },
                        {
                            headlineFirstLine: "Wonderful",
                            headlineSecondLine: "Roma",
                            sublineFirstLine: "Buon giorno",
                            sublineSecondLine: "buona giornata",
                            bgImg: RomaImage,
                            rectImg: RomaImage
                        },
                        {
                            headlineFirstLine: "Amazing",
                            headlineSecondLine: "Amsterdam",
                            sublineFirstLine: "Goedemorgen",
                            sublineSecondLine: "prettige dag",
                            bgImg: AmsterdamImage,
                            rectImg: AmsterdamImage
                        }
                    ],
        }
    },
  
                // mounted() {
                //         // var productRotatorSlide = document.getElementById("slider");
                //         var startX = 0;
                //         var endX = 0;

                        // productRotatorSlide.addEventListener(
                        // "touchstart",
                        // event => (startX = event.touches[0].pageX)
                        // );

                        // productRotatorSlide.addEventListener(
                        // "touchmove",
                        // event => (endX = event.touches[0].pageX) 
                        // );

                        // productRotatorSlide.addEventListener(
                        // "touchend",
                        // function(event) {
                        //     var threshold = startX - endX;

                        //     if (threshold < 150 && 0 < this.currentSlide) {
                        //     this.currentSlide--;
                        //     }
                        //     if (threshold > -150 && this.currentSlide < this.slides.length - 1) {
                        //     this.currentSlide++;
                        //     }
                        // }.bind(this)
                        // );
                        // this.startRotation();
                    // },
                    methods: {
                        updateSlide(index) {
                        index < this.currentSlide ? this.isPreviousSlide = true : this.isPreviousSlide = false;
                        this.currentSlide = index;
                        // this.isFirstLoad = false;
                        },
                        startRotation() {
                            this.timer = setInterval(this.next, 5000);
                        },
                        // next() {
                        //     setInterval(this.currentSlide < this.slides.length - 1 ? this.updateSlide(this.currentSlide + 1) : this.updateSlide(0), 5000);
                        // },
                        stopRotation() {
                        // clearTimeout(this.timer);
                        // this.timer = null;
                        }
                    }
            
    
  };

 

</script>
