<template>
  <section id="hero" class="hero">
    <div class="container hero-inner">
      <div class="hero-label fade-up" style="animation-delay:.1s">
        <span class="mono">Full-Stack Developer</span>
        <span class="dot">·</span>
        <span class="mono">10+ Years Experience</span>
      </div>
      <h1 class="hero-title fade-up" style="animation-delay:.25s">
        Building scalable<br/>
        <em>web solutions</em> that perform and last.
      </h1>
      <!-- Skills -->
      <div class="hero-cta fade-up flex gap-4 flex-wrap mb-8" style="animation-delay:.55s">
        <span class="px-4 py-2 rounded-full bg-purple-500/10 text-purple-400 border border-purple-400/30">
          TYPO3
        </span>
        <span class="px-4 py-2 rounded-full bg-green-500/10 text-green-400 border border-green-400/30">
          Laravel
        </span>
        <span class="px-4 py-2 rounded-full bg-blue-500/10 text-blue-400 border border-blue-400/30">
          Vue.js
        </span>
        <span class="px-4 py-2 rounded-full bg-yellow-500/10 text-yellow-400 border border-yellow-400/30">
          JavaScript
        </span>
      </div>
    
      <div class="flex gap-4 fade-up flex-wrap" style="animation-delay:.75s">
        <a href="#projects" class="px-6 py-3 rounded-full text-white font-medium 
        bg-gradient-to-r from-yellow-500 to-blue-500 
        hover:scale-105 transition duration-300">
          View Work →
        </a>
        <a :href="resumeUrl" target="_blank" class="px-6 py-3 rounded-full border border-gray-400 
        hover:bg-white hover:text-black transition duration-300 flex items-center gap-2">
          ⬇ Download Resume
        </a>
      </div>
    </div>

    <div class="hero-scroll">
      <span class="mono">Scroll</span>
      <div class="scroll-line"></div>
    </div>
  </section>
</template>
<script setup>
const resumeUrl = import.meta.env.BASE_URL + 'resume.pdf'
</script>

<style scoped>
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  position: relative;
  padding: 120px 0 80px;
}
.hero-inner { max-width: 860px; }

.hero-label {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 2.5rem;
}
.mono {
  font-family: var(--ff-mono);
  font-size: 0.85rem;
  letter-spacing: 0.08em;
  color: var(--muted);
}
.dot { color: var(--accent); font-size: 1rem; }

.hero-title {
  font-family: var(--ff-display);
  font-size: clamp(3.5rem, 7vw, 6.5rem);
  font-weight: 300;
  line-height: 1.1;
  letter-spacing: -0.01em;
  margin-bottom: 2rem;
}
.hero-title em {
  font-style: italic;
  color: var(--accent);
}

.hero-sub {
  font-size: 1rem;
  color: var(--muted);
  line-height: 1.8;
  margin-bottom: 3rem;
}

.hero-cta { display: flex; gap: 1.25rem; align-items: center; }

.btn-primary {
  display: inline-block;
  padding: 0.85rem 2.25rem;
  background: var(--ink);
  color: var(--paper);
  text-decoration: none;
  font-size: 0.78rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  transition: background 0.25s, transform 0.2s;
}
.btn-primary:hover { background: #2a2a26; transform: translateY(-1px); }

.btn-ghost {
  display: inline-block;
  color: var(--muted);
  text-decoration: none;
  font-size: 0.78rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  border-bottom: 1px solid var(--rule);
  padding-bottom: 2px;
  transition: color 0.2s, border-color 0.2s;
}
.btn-ghost:hover { color: var(--ink); border-color: var(--ink); }

.hero-scroll {
  position: absolute;
  bottom: 2.5rem;
  right: 2.5rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.75rem;
}
.scroll-line {
  width: 1px;
  height: 60px;
  background: linear-gradient(to bottom, var(--accent), transparent);
  animation: scrollPulse 2s ease-in-out infinite;
}
@keyframes scrollPulse {
  0%, 100% { opacity: 0.3; transform: scaleY(0.7); }
  50% { opacity: 1; transform: scaleY(1); }
}
</style>
