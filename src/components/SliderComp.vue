<script>
import sliderData from '../data/slider';
import TxtCard from './card/TxtCard.vue';

export default {
  name: 'SliderComp',
  components:{
    TxtCard
  },
  data() {
    return {
      slider: sliderData,
      currentImage: 0,
    };
  },
  computed: {
    currentSlide() {
      return this.slider[this.currentImage];
    },
  },
  methods: {
    nextImage() {
      this.currentImage = (this.currentImage + 1) % this.slider.length;
    },
    previousImage() {
      this.currentImage = (this.currentImage - 1 + this.slider.length) % this.slider.length;
    },
  },
};
</script>


<template>
  <div class="image-slider">
    <div class="slider-container">
      <transition name="fade" mode="out-in">
        <img :key="currentImage" :src="currentSlide.imageSrc" :alt="currentSlide.imageAlt" />
      </transition>
      <div class="card-overlay">
        <TxtCard class="card"
        :heading="currentSlide.heading"
        :ltlPrice="currentSlide.price"
        :description="currentSlide.content"
        :buttonText=" currentSlide.buttonText"
        />

      </div>
    </div>
    <div class="controls">
      <button @click="previousImage">Prev</button>
      <button @click="nextImage">Next</button>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.image-slider {
  margin: 60px 0;
  position: relative;

  .slider-container {
    height: 900px;

    img {
      object-fit: contain;
    }
  }

  .card-overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;

    .card {
      background-color: rgba(0, 0, 0);
      color: white;
      padding: 10px 20px;
      height: 80%;
      width: 450px;
      margin-left: 220px;
    }
  }

  .controls {
    position: absolute;
    bottom: 50%;
    z-index: 999;
    display: flex;
    justify-content: space-between;
    width: 100%;
    padding: 15px;

    button {
      background-color: grey;
      color: white;
      padding: 10px 20px;
      border-radius: 5px;

      &:hover{
        background-color: white;
        color: grey;
      }
    }

    .prev-button {
      margin-right: 10px;
    }
  }
}
</style>
