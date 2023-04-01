<template>

  <h2 class="text-center text-lg lg:text-2xl tracking-widest text-white lg:text-left lg:ml-20 mb-5">
      <span class="text-gray-600">01</span>
        meet your crew
  </h2>
  <div class="w-4/5 mx-auto">
    <div
      v-for="(slide, index) in slides"
      :key="index"
      class="flex flex-col justify-center items-center m-auto gap-4 lg:flex-row lg:w-full lg:justify-between mySlides fade"
      v-show="index === slideIndex - 1"
    >
      <div class=" img mt-4 lg:mt-0 lg:order-1 lg:w-2/5">
        <img :src="`_nuxt` + slide.images.png" :alt="slide.imgAlt" class="w-4/4 mx-auto max-h-" />
      </div>
      <div class="flex flex-col justify-center items-center lg:gap-2 lg:w-2/5 lg:items-start lg:max-h-80">
        
        <div class="dots lg:order-none">
          <span
            class="dot lg:order-none"
            v-for="(slide, index) in slides"
            :key="index"
            @click="currentSlide(index)"
            :class="{ active: index === slideIndex - 1 }"
          ></span>
        </div>
        <div class="text-center flex flex-col gap-2 lg:text-left lg:order-1">
          <h3 class="uppercase text-gray-400 text-xl font-normal lg:text-3xl">{{ slide.role }}</h3>
          <h1 class="uppercase text-gray-100 text-3xl font-light lg:text-5xl">{{ slide.name }}</h1>
          <p class="uppercase text-gray-500 text-base font-light lg:text-xl  lg:mt-5">{{ slide.bio }}</p>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>
import { ref, onMounted } from 'vue';
import data from '../data.json'

const slides =  data.crew

const slideIndex = ref(slides.length);

function currentSlide(index) {
  slideIndex.value = index + 1;
  showSlides()
}

function plusSlides(n) {
  slideIndex.value += n;
  console.log(n)
  if (slideIndex.value < 1) {
    slideIndex.value = slides.length;
  } else if (slideIndex.value > slides.length) {
    slideIndex.value = 1;
  }
   showSlides();
}

function showSlides() {
  const slideElems = document.querySelectorAll('.mySlides');
  const dotElems = document.querySelectorAll('.dot');

  slideElems.forEach((slide) => {
    slide.style.display = 'none';
  });

  dotElems.forEach((dot) =>{
    dot.className = dot.className.replace(' active', '');
  });

  slideElems[slideIndex.value - 1].style.display = 'block';
  dotElems[slideIndex.value - 1].className += ' active';
}

onMounted(() => {
showSlides();
});

</script>

<style scoped>
.img {
  border-bottom: 1px #777 solid;
}
/* The dots/bullets/indicators */
.dots {
    text-align: center;
}

.dot {
  cursor: pointer;
  height: 10px;
  width: 10px;
  margin: 0 10px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active, .dot:hover {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

</style>

