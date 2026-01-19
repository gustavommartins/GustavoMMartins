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
    role: 'Engenheiro de software',
    period: 'nov 2021 — Presente',
    project: 'Itaú',
    projectUrl: 'https://www.itau.com.br/',
    technologies: ['Java', 'Spring Boot', 'Kafka', 'Microservices']
  },
  {
    company: 'DXC Technology',
    companyUrl: 'https://dxc.com/br/pt',
    role: 'Engenheiro de software',
    period: 'mai 2021 — nov 2021',
    project: 'Petrobras',
    projectUrl: 'https://petrobras.com.br/',
    technologies: ['Java', 'Spring Boot', 'JUnit', 'Angular']
  },
  {
    company: 'Lumis',
    companyUrl: 'https://www.lumis.com.br/',
    role: 'Desenvolvedor Web/Java',
    period: 'nov 2020 — mar 2021',
    project: 'Lumis XP',
    projectUrl: 'https://www.lumis.com.br/',
    technologies: ['Java', 'Angular', 'CSS', 'Desenvolvimento web']
  },
  {
    company: 'Mestra Informática',
    companyUrl: 'https://mestrainfo.com.br/site/',
    role: 'Desenvolvedor Web/Java',
    period: 'jul 2020 — nov 2020',
    project: 'Prevdata',
    projectUrl: 'https://www.prevdata.org.br/',
    technologies: ['Java', 'Struts', 'JSP', 'SQL Server']
  },
  {
    company: 'Mestra Informática',
    companyUrl: 'https://mestrainfo.com.br/site/',
    role: 'Desenvolvedor Web/Java (Estágio)',
    period: 'fev 2019 — jul 2020',
    project: 'Prevdata',
    projectUrl: 'https://www.prevdata.org.br/',
    technologies: ['Java', 'MVC', 'Desenvolvimento web']
  }
]
</script>
