<template>
  <section id="certifications" class="py-24 px-6 bg-white">
    <div class="max-w-xl mx-auto">
      <p class="section-title">Certificações</p>
      
      <div class="space-y-6">
        <a v-for="cert in certifications" :key="cert.id" 
           :href="cert.badgeUrl" target="_blank" rel="noopener noreferrer"
           class="flex items-center gap-4 group">
          <img :src="cert.image" :alt="cert.name" 
               class="w-12 h-12 rounded grayscale group-hover:grayscale-0 transition-all" />
          <div>
            <h3 class="text-sm font-medium text-stone-700 group-hover:text-stone-900">{{ cert.name }}</h3>
            <p class="text-xs text-stone-400">{{ cert.issuer }} · {{ cert.year }}</p>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>

<script setup>
const certifications = [
  {
    id: 1,
    name: 'AWS Certified Cloud Practitioner',
    issuer: 'Amazon Web Services',
    year: '2023',
    image: 'https://images.credly.com/size/340x340/images/00634f82-b07f-4bbd-a6bb-53de397fc3a6/image.png',
    badgeUrl: 'https://www.credly.com/earner/earned/badge/b808850c-6cf7-4276-8c5a-d21222c6656f'
  },
  {
    id: 2,
    name: 'AWS Solutions Architect – Associate',
    issuer: 'Amazon Web Services',
    year: '2024',
    image: 'https://images.credly.com/size/340x340/images/0e284c3f-5164-4b21-8660-0d84737941bc/image.png',
    badgeUrl: 'https://www.credly.com/badges/a91c740a-418a-4786-9fd2-e39fdc207a13'
  }
]
</script>
