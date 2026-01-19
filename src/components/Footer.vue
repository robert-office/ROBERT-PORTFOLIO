<script setup>

</script>

<template>
  <footer class="border-t border-neutral-800/50 bg-[#18181b] mt-20">
    <div class="container mx-auto px-4 py-12">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-8">
        
        <!-- Logo e descrição -->
        <div>
          <h3 class="text-2xl text-neutral-200 font-gravitas mb-3">Robert U.</h3>
          <p class="text-neutral-400 font-roboto text-sm leading-relaxed">
            Desenvolvedor Full Stack especializado em criar soluções web modernas e escaláveis.
          </p>
        </div>

        <!-- Links rápidos -->
        <div>
          <h4 class="text-neutral-200 font-oswald text-lg font-bold mb-4">Links Rápidos</h4>
          <ul class="space-y-2">
            <li>
              <a href="#topo" class="text-neutral-400 hover:text-purple-400 font-roboto text-sm transition-colors duration-300">Início</a>
            </li>
            <li>
              <a href="#sobremim" class="text-neutral-400 hover:text-purple-400 font-roboto text-sm transition-colors duration-300">Sobre Mim</a>
            </li>
            <li>
              <a href="#projetos" class="text-neutral-400 hover:text-purple-400 font-roboto text-sm transition-colors duration-300">Projetos</a>
            </li>
          </ul>
        </div>

        <!-- Redes sociais -->
        <div>
          <h4 class="text-neutral-200 font-oswald text-lg font-bold mb-4">Contato</h4>
          <div class="flex gap-4">
            <a
              href="https://wa.me/5511983521013?text=Olá!%20Gostaria%20de%20conversar%20sobre%20um%20projeto"
              target="_blank"
              rel="noopener noreferrer"
              class="w-10 h-10 bg-neutral-800 hover:bg-green-500 rounded-full flex items-center justify-center transition-all duration-300 hover:scale-110"
            >
              <font-awesome-icon :icon="['fab', 'whatsapp']" class="text-neutral-300 hover:text-white" />
            </a>
            <a 
              href="https://github.com/robert-office"
              target="_blank" 
              rel="noopener noreferrer"
              class="w-10 h-10 bg-neutral-800 hover:bg-purple-500 rounded-full flex items-center justify-center transition-all duration-300 hover:scale-110"
            >
              <font-awesome-icon :icon="['fab', 'github']" class="text-neutral-300 hover:text-white" />
            </a>
            <a 
              href="https://linkedin.com/in/robertuillians"
              target="_blank" 
              rel="noopener noreferrer"
              class="w-10 h-10 bg-neutral-800 hover:bg-purple-500 rounded-full flex items-center justify-center transition-all duration-300 hover:scale-110"
            >
              <font-awesome-icon :icon="['fab', 'linkedin']" class="text-neutral-300 hover:text-white" />
            </a>
          </div>
        </div>

      </div>

      <!-- Copyright -->
      <div class="border-t border-neutral-800 pt-6">
        <p class="text-neutral-500 font-roboto text-sm text-center">
          © {{ new Date().getFullYear() }} Robert U. Todos os direitos reservados.
        </p>
      </div>
    </div>
  </footer>
</template>

<style scoped>

</style>
