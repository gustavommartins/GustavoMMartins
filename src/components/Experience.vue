<template>
  <section id="experience" class="py-24 px-6">
    <div class="max-w-xl mx-auto">
      <p class="section-title">Trabalho</p>
      
      <div class="space-y-10">
        <article v-for="(exp, index) in experiences" :key="index">
          <div class="flex items-baseline justify-between gap-4 mb-2">
            <h3 class="font-medium text-stone-800">{{ exp.role }}</h3>
            <span class="text-xs text-stone-400 whitespace-nowrap">{{ exp.period }}</span>
          </div>
          
          <a :href="exp.companyUrl" target="_blank" rel="noopener noreferrer"
             class="text-sm text-stone-500 hover:text-stone-700 transition-colors">
            {{ exp.company }} →
          </a>
          
          <p v-if="exp.project" class="mt-3 text-sm text-stone-500">
            Projeto: <a :href="exp.projectUrl" target="_blank" rel="noopener noreferrer" 
                        class="text-stone-700 hover:underline">{{ exp.project }}</a>
          </p>
          
          <p class="mt-3 text-xs text-stone-400">
            {{ exp.technologies.join(' · ') }}
          </p>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    company: 'BRQ Digital Solutions',
    companyUrl: 'https://www.brq.com/',
    role: 'Software Engineer',
    period: '2024 — Presente',
    project: 'Itaú',
    projectUrl: 'https://www.itau.com.br/',
    technologies: ['Java', 'AWS', 'Docker', 'Microservices']
  },
  {
    company: 'DXC Technology',
    companyUrl: 'https://dxc.com/br/pt',
    role: 'Software Engineer',
    period: '2023 — 2024',
    project: 'Petrobras',
    projectUrl: 'https://petrobras.com.br/',
    technologies: ['Java', 'Angular', 'Oracle DB', 'Docker']
  },
  {
    company: 'Lumis',
    companyUrl: 'https://www.lumis.com.br/',
    role: 'Full-Stack Developer',
    period: '2022 — 2023',
    project: 'Previ',
    projectUrl: 'https://www.previ.com.br/portal-previ/',
    technologies: ['Java', 'Angular', 'Oracle', 'Docker']
  },
  {
    company: 'Mestra Informática',
    companyUrl: 'https://mestrainfo.com.br/site/',
    role: 'Full-Stack Developer',
    period: '2020 — 2022',
    project: 'Prevdata',
    projectUrl: 'https://www.prevdata.org.br/',
    technologies: ['Java', 'Angular', 'SQL Server', 'Oracle']
  }
]
</script>
