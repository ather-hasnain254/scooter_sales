<template>
  <section class="bg-[#1a1a2e] py-16">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-center text-3xl sm:text-4xl font-extrabold text-white uppercase tracking-widest mb-10">
        Our Models
      </h2>

      <!-- Carousel -->
      <div class="relative overflow-hidden rounded-xl shadow-2xl">
        <div class="flex transition-transform duration-500 ease-in-out"
             :style="{ transform: `translateX(-${current * 100}%)` }">
          <div v-for="(slide, index) in slides" :key="index"
               class="min-w-full relative">
            <img :src="slide.image" :alt="slide.name" class="w-full h-64 sm:h-80 md:h-96 object-cover"/>
            <div class="absolute inset-0 bg-gradient-to-t from-black/70 to-transparent flex items-end p-6">
              <span class="text-white text-2xl font-bold uppercase tracking-widest">{{ slide.name }}</span>
            </div>
          </div>
        </div>

        <!-- Prev/Next -->
        <button @click="prev"
          class="absolute left-3 top-1/2 -translate-y-1/2 bg-black/50 hover:bg-black/75 text-white rounded-full p-2 transition-colors">
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"/>
          </svg>
        </button>
        <button @click="next"
          class="absolute right-3 top-1/2 -translate-y-1/2 bg-black/50 hover:bg-black/75 text-white rounded-full p-2 transition-colors">
          <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>

      <!-- Dots -->
      <div class="flex justify-center mt-6 space-x-2">
        <button v-for="(slide, index) in slides" :key="index"
          @click="goTo(index)"
          :class="['w-3 h-3 rounded-full transition-colors duration-200', current === index ? 'bg-[#c41e3a]' : 'bg-white/40 hover:bg-white/70']">
        </button>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const slides = [
  { name: 'Buddy', image: 'https://picsum.photos/seed/scooter_buddy/900/500' },
  { name: 'Roughhouse', image: 'https://picsum.photos/seed/scooter_rough/900/500' },
  { name: 'Hooligan', image: 'https://picsum.photos/seed/scooter_hool/900/500' },
  { name: 'Blur', image: 'https://picsum.photos/seed/scooter_blur/900/500' },
]

const current = ref(0)

function next() {
  current.value = (current.value + 1) % slides.length
}
function prev() {
  current.value = (current.value - 1 + slides.length) % slides.length
}
function goTo(index) {
  current.value = index
}

let timer
onMounted(() => {
  timer = setInterval(next, 4000)
})
onUnmounted(() => {
  clearInterval(timer)
})
</script>
