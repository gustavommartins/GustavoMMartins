<template>
  <footer class="py-12 px-6 border-t border-stone-200">
    <div class="max-w-xl mx-auto">
      <div class="flex flex-col sm:flex-row justify-between items-center gap-4 text-xs text-stone-400">
        <p>© {{ currentYear }} Gustavo Martins</p>
        <p>Feito com Vue.js + Tailwind</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { ref } from 'vue'

const currentYear = ref(new Date().getFullYear())
</script>
