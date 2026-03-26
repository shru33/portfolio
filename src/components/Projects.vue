<template>
  <section id="projects" class="py-30">
    <div class="container">
      <header class="section-header">
        <p class="section-label mono">03 / Selected Work</p>
        <h2 class="section-title">Projects that<br/><em>define</em> the work.</h2>
      </header>
      <div
      v-for="(project, index) in projects"
      :key="project.id"
      class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center py-12 border-t border-gray-100 dark:border-gray-800 last:border-b"
      :class="{ 'md:[direction:rtl]': index % 2 !== 0 }"
    >
      <!-- Content -->
      <div :class="{ 'md:[direction:ltr]': index % 2 !== 0 }">
        <h3 class="text-xl font-semibold text-gray-900 dark:text-white tracking-tight mb-3">
          {{ project.title }}
        </h3>
        <p class="text-gray-600 leading-relaxed mb-5">
          {{ project.description }}
        </p>

        <!-- Key Features -->
        <!--
        <p class="font-mono text-[10px] tracking-widest uppercase text-gray-400 mb-2">Key Features</p>
        <div class="grid grid-cols-2 gap-y-2 gap-x-4 mb-5">
          <div
            v-for="feature in project.features"
            :key="feature"
            class="flex items-center gap-2 text-sm text-gray-500 dark:text-gray-400"
          >
            <span class="w-1.5 h-1.5 rounded-full bg-amber-500 flex-shrink-0"></span>
            {{ feature }}
          </div>
        </div>
        -->

        <!-- Technologies -->
        <p class="font-mono text-[10px] tracking-widest uppercase text-gray-400 mb-2">Technologies</p>
        <div class="flex flex-wrap gap-2 mb-5">
          <span
            v-for="tech in project.techs"
            :key="tech"
            class="font-mono text-xs px-3 py-1 rounded-full border border-gray-200 dark:border-gray-700 text-gray-500 dark:text-gray-400"
          >
            {{ tech }}
          </span>
        </div>

        <!-- Link -->
        <a
          :href="project.link"
          target="_blank"
          class="inline-flex items-center gap-1.5 text-sm font-medium text-gray-900 dark:text-white border-b border-gray-300 dark:border-gray-600 pb-0.5 hover:border-gray-900 dark:hover:border-white transition-colors"
        >
          <svg class="w-3.5 h-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
            <path d="M18 13v6a2 2 0 01-2 2H5a2 2 0 01-2-2V8a2 2 0 012-2h6"/>
            <polyline points="15 3 21 3 21 9"/>
            <line x1="10" y1="14" x2="21" y2="3"/>
          </svg>
          Visit Project
        </a>
      </div>

      <!-- Image -->
      <div
        class="rounded-lg overflow-hidden border border-gray-100 dark:border-gray-800 bg-gray-50 dark:bg-gray-900"
        :class="{ 'md:[direction:ltr]': index % 2 !== 0 }"
      >
        <img
          :src="project.image"
          :alt="project.title"
          class="w-full aspect-video object-cover object-top"
        />
      </div>
    </div>
    </div>
    
    
  </section>
</template>

<script setup>
const baseUrl = import.meta.env.BASE_URL

const projects = [
  {
    id: 1,
    title: 'ASMR Stars® – ASMR Video Platform',
    description: 'The #1 ASMR Video Content Creator Platform! Earn with ASMR videos, get more fans and connect with top ASMR creators.',
    techs: ['Laravel', 'Vue js', 'Bootstrap'],
    image: `${baseUrl}projects/asmr.jpg`,
    link: 'https://asmrstars.com/'
  },
  {
    id: 2,
    title: 'Resume Builder',
    description: 'A browser-based resume builder with real-time preview and one-click PDF export. No login, no friction — just fill in your details and download.',
    techs: ['Vue js'],
    image: `${baseUrl}projects/resume-builder.jpg`,
    link: 'https://shru33.github.io/resume-builder/'
  },
  {
    id: 3,
    title: 'Lewero',
    description: 'Electricity & Gas for Businesses. Whether SME, Retail, Grocery, or Property Management.',
    techs: ['Typo3', 'Extbase', 'jQuery'],
    image: `${baseUrl}/projects/lewero.jpg`,
    link: 'https://lewero.de/'
  },
  {
    id: 4,
    title: 'Bestattungen Fraund/Amelung in Wiesbaden',
    description: 'Bestattungen Fraund/Amelung in Wiesbaden offers all services related to funerals and funeral pre-planning',
    techs: ['Typo3', 'Extbase', 'jQuery'],
    image: `${baseUrl}/projects/fraund-amelung.jpg`,
    link: 'https://fraund-amelung.de/'
  },
  {
    id: 5,
    title: 'Property Management System',
    description: 'Designed and delivered a user-friendly property management solution that simplifies day-to-day operations for small to medium property owners',
    techs: ['Laravel', 'AdminLte'],
    image: `${baseUrl}projects/whitehouse.jpg`,
    link: '#'
  },
  {
    id: 6,
    title: 'Senckenberg Turm',
    description: 'With the Senckenberg Tower, a new and exciting era begins in Frankfurt. A well-known location is reinventing itself and becoming a communicative hub for work, life, lifestyle, hotel, leisure, and culture',
    techs: ['Typo3', 'Extbase', 'jQuery'],
    image: `${baseUrl}projects/senckenbergturm.jpg`,
    link: 'https://senckenbergturm.de'
  },
  {
    id: 7,
    title: 'YORCKS CAMPUS',
    description: 'YORCKS offers ideal office spaces in Düsseldorf to connect with others. Rental space for offices, training, retail, fitness, and gastronomy',
    techs: ['Typo3', 'Extbase', 'jQuery'],
    image: `${baseUrl}projects/yorcks.jpg`,
    link: 'https://www.yorcks.com/'
  }
]
</script>

<style scoped>

.section-label { color: var(--muted); display: block; margin-bottom: 1.5rem; }
.section-title {
  font-family: var(--ff-display);
  font-size: clamp(2.2rem, 4vw, 3.5rem);
  font-weight: 300;
  line-height: 1.15;
}
.section-title em { font-style: italic; color: var(--accent); }
</style>