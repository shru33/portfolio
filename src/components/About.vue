<template>
  <section id="about" class="about">
    <div class="container max-w-6xl mx-auto grid md:grid-cols-2 gap-12">
      <div class="about-left">
        <p class="section-label mono">02 / About</p>
        <!--
        <p class="text-gray-600 mb-4">
          I am a Senior Full-Stack Developer with 10+ years of experience 
          building scalable and high-performance web applications.
        </p>

        <p class="text-gray-600 mb-6">
          I specialize in Laravel, TYPO3, and modern frontend technologies, 
          focusing on clean architecture and real-world solutions.
        </p>
        -->

        <!-- Tech Stack -->
        <div class="flex flex-wrap gap-3">
          <span class="px-3 py-1 bg-black text-white rounded-full text-sm">Laravel</span>
          <span class="px-3 py-1 bg-gray-800 text-white rounded-full text-sm">TYPO3</span>
          <span class="px-3 py-1 bg-gray-700 text-white rounded-full text-sm">Vue.js</span>
          <span class="px-3 py-1 bg-gray-600 text-white rounded-full text-sm">JavaScript</span>
          <span class="px-3 py-1 bg-gray-500 text-white rounded-full text-sm">jQuery</span>
          <span class="px-3 py-1 bg-gray-500 text-white rounded-full text-sm">HTML5</span>
          <span class="px-3 py-1 bg-gray-500 text-white rounded-full text-sm">CSS3</span>
          <span class="px-3 py-1 bg-gray-500 text-white rounded-full text-sm">MySQL</span>
        </div>
      </div>
      <div class="about-right">
        <p>
          Senior Full Stack Developer with 10 years of experience specializing in TYPO3 CMS development, custom extension development, TYPO3 upgrades, and performance improvements. Experienced in developing responsive, accessible user interfaces using HTML, CSS, JavaScript, jQuery and Bootstrap, with hands-on experience in third-party API integration.
        </p>
        <p>
          Hands-on experience in Laravel development, including user & role management (RBAC) and CRUD applications using Blade and Eloquent ORM. Basic exposure to Vue.js for frontend components in Laravel-based applications.
        </p>
        <div class="about-facts">
          <div class="fact">
            <span class="fact-num">10+</span>
            <span class="fact-label mono">Years exp.</span>
          </div>
          <div class="fact">
            <span class="fact-num">40+</span>
            <span class="fact-label mono">Projects</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  padding: 120px 0;
}
.section-label {
  color: var(--muted);
  margin-bottom: 2rem;
  display: block;
}
.about-heading {
  font-family: var(--ff-display);
  font-size: clamp(2rem, 3.5vw, 3rem);
  font-weight: 300;
  line-height: 1.2;
  position: sticky;
  top: 100px;
}
.about-heading em { font-style: italic; color: var(--accent); }

.about-right p {
  font-size: 1rem;
  line-height: 1.85;
  color: #3a3a36;
  margin-bottom: 1.5rem;
}
.about-right strong { font-weight: 500; color: var(--ink); }

.about-facts {
  display: flex;
  gap: 3rem;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid var(--rule);
}
.fact { display: flex; flex-direction: column; gap: 0.25rem; }
.fact-num {
  font-family: var(--ff-display);
  font-size: 2.5rem;
  font-weight: 300;
  color: var(--ink);
  line-height: 1;
}
.fact-label { color: var(--muted); font-size: 0.7rem; letter-spacing: 0.08em; }

@media (max-width: 768px) {
  .about-grid { grid-template-columns: 1fr; gap: 3rem; }
  .about-heading { position: static; }
}
</style>
