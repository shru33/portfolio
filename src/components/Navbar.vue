<template>
  <header :class="['nav', { scrolled }]">
    <div class="container nav-inner flex justify-between">
      <a href="#hero" class="nav-logo">Shruti Hegde</a>
      <nav class="nav-links">
        <a href="#about">About</a>
        <a href="#projects">Work</a>
        <a href="#skills">Skills</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
const scrolled = ref(false)
const onScroll = () => { scrolled.value = window.scrollY > 40 }
onMounted(() => window.addEventListener('scroll', onScroll))
onUnmounted(() => window.removeEventListener('scroll', onScroll))
</script>

<style scoped>
.nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  transition: background 0.4s, border-color 0.4s;
  border-bottom: 1px solid transparent;
}
.nav.scrolled {
  background: rgba(244,241,235,0.92);
  backdrop-filter: blur(12px);
  border-color: var(--rule);
}
.nav-inner {
  align-items: center;
  height: 64px;
}
.nav-logo {
  font-family: var(--ff-display);
  font-size: 1.25rem;
  font-weight: 400;
  letter-spacing: 0.02em;
  color: var(--ink);
  text-decoration: none;
}
.nav-links {
  display: flex;
  gap: 2.5rem;
}
.nav-links a {
  font-size: 0.75rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  text-decoration: none;
  transition: color 0.2s;
}
.nav-links a:hover { color: var(--ink); }
</style>