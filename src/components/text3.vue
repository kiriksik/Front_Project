<script setup>

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

const slides = [
  { id: '1', src: 'src\\components\\imgs\\img1.png' },
  { id: '2', src: 'src\\components\\imgs\\img2.png' },
  { id: '3', src: 'src\\components\\imgs\\img3.png' },
  { id: '4', src: 'src\\components\\imgs\\img4.png' },
  { id: '5', src: 'src\\components\\imgs\\img5.png' }
];

</script>

<template>

    <div class="slaider">
      <Carousel>
        <Slide v-for="slide in slides" :key="slide.id">
          <div class="carousel__item">
            <img :src='slide.src'>
          </div>
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
    </div>
  
</template>


<style>
  .slaider {
    margin-left:10%;
    margin-right: 10%;
  }

  .carousel__item, img {
  min-height: 200px;
  width: 100%;
  background-color: white;
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
}

</style>
