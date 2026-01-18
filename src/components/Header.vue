<template>
  <header class="fixed top-0 left-0 right-0 z-50 bg-stone-50/90 backdrop-blur-sm">
    <nav class="max-w-xl mx-auto px-6 py-5">
      <div class="flex justify-center items-center">
        <div class="hidden md:flex items-center gap-8">
          <a v-for="item in menuItems" :key="item.href" :href="item.href"
             class="text-xs text-stone-400 hover:text-stone-800 transition-colors">
            {{ item.label }}
          </a>
        </div>
        
        <button @click="toggleMenu" class="md:hidden">
          <svg class="w-4 h-4 text-stone-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path v-if="!mobileMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M4 6h16M4 12h16"></path>
            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M6 18L18 6M6 6l12 12"></path>
          </svg>
        </button>
      </div>
      
      <div v-if="mobileMenuOpen" class="md:hidden mt-6 space-y-4 text-center">
        <a v-for="item in menuItems" :key="item.href" :href="item.href" @click="toggleMenu"
           class="block text-sm text-stone-500 hover:text-stone-800">
          {{ item.label }}
        </a>
      </div>
    </nav>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const menuItems = [
  { label: 'Sobre', href: '#about' },
  { label: 'Trabalhos', href: '#experience' },
  { label: 'Stack', href: '#skills'},
  { label: 'Contato', href: '#contact' }
]

const toggleMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
}
</script>
