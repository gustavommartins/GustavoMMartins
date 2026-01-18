<template>
  <section id="about" class="min-h-[90vh] flex items-center px-6 pt-20">
    <div class="max-w-xl mx-auto">
      <div class="mb-8 flex justify-center">
        <img 
          src="/GustavoMMartins/empresas/perfil.webp" 
          alt="Gustavo Martins"
          class="w-24 h-24 rounded-full grayscale hover:grayscale-0 transition-all duration-700 cursor-pointer"
        />
      </div>
      
      <h1 class="text-3xl md:text-4xl font-normal text-stone-800 mb-6 leading-tight">
        Olá, sou <span class="font-semibold">Gustavo</span>
      </h1>
      
      <div class="space-y-6 text-base text-stone-600 leading-relaxed mb-6">
        <p>
          Desenvolvedor há mais de 6 anos, trabalhando com Java, Spring Boot 
          e serviços na nuvem da AWS. Gosto de código limpo, arquitetura bem pensada 
          e soluções que realmente resolvem problemas.
        </p>
        
        <p>
          Já passei por projetos em empresas como Itaú, Petrobras e Previ — 
          sempre focado em microsserviços, APIs REST e práticas DevOps.
        </p>
      </div>
      
      <div class="flex items-center gap-x-8 gap-y-2 flex-wrap text-sm text-stone-400 mb-8">
        <span>Joinville, SC</span>
        <span>+6 anos exp.</span>
        <span>2 certs AWS</span>
      </div>
      
      <div class="flex items-center gap-6 text-sm">
        <a href="https://github.com/gustavommartins" 
           target="_blank" rel="noopener noreferrer"
           class="text-stone-400 hover:text-stone-800 transition-colors">
          GitHub
        </a>
        <a href="https://www.linkedin.com/in/gustavo-martins-7170a419a/" 
           target="_blank" rel="noopener noreferrer"
           class="text-stone-400 hover:text-stone-800 transition-colors">
          LinkedIn
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>
