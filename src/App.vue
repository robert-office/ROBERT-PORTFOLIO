<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Topbar from "@/components/Topbar.vue";
import Hero from "@/components/Hero.vue";
import Sobre from "@/components/Sobre.vue";
import Projetos from "@/components/Projetos.vue";
import CTA from "@/components/CTA.vue";
import Footer from "@/components/Footer.vue";

const showScrollTop = ref(false)

const handleScroll = () => {
  showScrollTop.value = window.scrollY > 300
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <div>
    <section id="topo">
      <Topbar/>

      <div class="sm:mt-20 mt-6">
        <Hero/>
      </div>

      <div class="sm:mt-20 mt-8">
        <Sobre/>
      </div>

      <div class="mt-8" id="projetos">
        <Projetos/>
      </div>

      <div class="mt-8">
        <CTA/>
      </div>

      <a 
        v-show="showScrollTop"
        href="#topo" 
        class="absolute sticky bottom-4 ml-auto mr-4 w-16 h-16 bg-neutral-800 rounded-full flex items-center justify-center cursor-pointer transition-all duration-300 hover:bg-neutral-700 hover:scale-110"
      >
        <font-awesome-icon :icon="['far', 'circle-up']" class="text-white text-3xl" />
      </a>
    </section>

    <Footer/>
  </div>
</template>

<style scoped></style>
