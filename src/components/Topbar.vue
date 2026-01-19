<template>
  <header class="sticky top-0 z-50 backdrop-blur-md bg-black/30 border-b border-neutral-800/50 py-4 sm:py-2">
    <div class="container mx-auto pt-4 pb-4 flex gap-6 items-center h-10 px-4">

    <section class="flex items-center gap-6 h-6">
      <p 
        @click="handleEasterEgg" 
        class="text-2xl text-neutral-300 font-light cursor-pointer hover:text-neutral-100 font-gravitas select-none"
      >
        Robert U.
      </p>
      <span class="sm:block hidden bg-gray-400 font-bold h-full w-0.5"></span>
    </section>

    <section class="items-center gap-8 h-6 sm:flex hidden">
      <a href="#sobremim" class="text-1xl text-neutral-300 font-medium cursor-pointer hover:text-neutral-100 font-roboto">SOBRE MIM</a>
      <a href="#projetos" class="text-1xl text-neutral-300 font-medium cursor-pointer hover:text-neutral-100 font-roboto">PROJETOS</a>
    </section>

    <section class="ml-auto">
      <a href="https://wa.me/5511983521013?text=Olá!%20Gostaria%20de%20conversar%20sobre%20um%20projeto" target="_blank" rel="noopener noreferrer" class="sm:rounded-none transition-all duration-300 ease-out hover:scale-105 hover:rotate-2 hover:shadow-md hover:shadow-green-500/30 rounded-full p-2 flex items-center gap-2 bg-neutral-300 text-neutral-900 font-medium cursor-pointer hover:bg-neutral-100 font-roboto">
        CONTATO
        <span class="relative flex h-5 w-5">
          <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75"></span>
          <font-awesome-icon :icon="['fab', 'whatsapp']" class="mt-0.5 relative text-green-500" />
        </span>
      </a>
    </section>
    </div>
  </header>

  <!-- Easter Egg Video Modal -->
  <div 
    v-if="showVideo" 
    @click="closeVideo"
    class="fixed inset-0 z-[9999] bg-black flex items-center justify-center cursor-pointer"
  >
    <div class="w-full h-full flex items-center justify-center p-4">
      <iframe 
        class="w-full h-full max-w-7xl max-h-[90vh]"
        src="https://www.youtube.com/embed/QTpmSALDqTE?autoplay=1" 
        title="Easter Egg" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen
      ></iframe>
    </div>
    <button 
      @click="closeVideo"
      class="absolute top-8 right-8 text-white text-4xl hover:text-red-500 transition-colors duration-300"
    >
      ×
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const clickCount = ref(0)
const showVideo = ref(false)

const handleEasterEgg = () => {
  clickCount.value++
  
  if (clickCount.value === 10) {
    showVideo.value = true
    clickCount.value = 0
  }
}

const closeVideo = () => {
  showVideo.value = false
}
</script>