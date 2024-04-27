<script setup>

import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

const slides = [
  { id: '1', src: 'src\\components\\imgs\\img1.jpg' },
  { id: '2', src: 'src\\components\\imgs\\img2.jpg' },
  { id: '3', src: 'src\\components\\imgs\\img3.jpg' },
  { id: '4', src: 'src\\components\\imgs\\img4.jpg' },
  { id: '5', src: 'src\\components\\imgs\\img5.jpg' },
  { id: '6', src: 'src\\components\\imgs\\img6.jpg' },
  { id: '7', src: 'src\\components\\imgs\\img7.jpg' },
  { id: '8', src: 'src\\components\\imgs\\img8.jpg' }
];

const PCslides = [
  { id: '1', src: 'src\\components\\imgs\\pc1.jpg' },
  { id: '2', src: 'src\\components\\imgs\\pc2.jpg' },
  { id: '3', src: 'src\\components\\imgs\\pc3.jpg' },
  { id: '4', src: 'src\\components\\imgs\\pc4.jpg' },
  { id: '5', src: 'src\\components\\imgs\\pc5.jpg' }
];

</script>

<template>
  <div class="flex">
    <h1 class="title">
        Наши товары
    </h1>
    <h1 class="title">
        Наши сборки
      </h1>
  </div>
  <div class="flex">
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

    <div class="slaider">
      <Carousel>
        <Slide v-for="slide in PCslides" :key="slide.id">
          <div class="carousel__item">
            <img :src='slide.src'>
          </div>
        </Slide>

        <template #addons>
          <Navigation />
        </template>
      </Carousel>
    </div>
  </div>
  
</template>


<style>


  .flex {
    display: flex;
    justify-content: center;
    flex-wrap: nowrap;
  }
  .title {
    padding-top: 20px;
    text-align: center;
    padding-left: 7%;
    text-transform: uppercase;
    font-weight: 100;
    line-height: 2;
    color: #2c3e50;
    width: 50%;
  }
  .slaider {
    width: 50%;
  }

  .carousel__item, img {
  min-height: auto;
  width: 60%;
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
