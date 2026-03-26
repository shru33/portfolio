<template>
  <section id="contact" class="contact py-30">
    <div class="container contact-inner">
      <p class="section-label mono">05 / Contact</p>
      <h2 class="contact-heading">Get In Touch</h2>
      <p class="text-gray-600 mb-4">
        Good projects start with good conversations. If you're working on something interesting <br> — or hiring — I'd genuinely love to hear about it.
      </p>

      <!-- Info block (like your reference image) -->
      <div class="flex flex-col gap-4 mb-10">
        
      </div>

      <!-- Social links -->
      <div class="flex flex-col gap-3 items-start">
        <a
          href="tel:+917892994174"
          class="flex items-center gap-3 text-gray-600 hover:text-gray-900 transition-colors group"
        >
          <span class="flex items-center justify-center w-9 h-9 rounded-full border border-gray-200 text-gray-400 group-hover:border-gray-400 group-hover:text-gray-600 transition-all">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 6.75c0 8.284 6.716 15 15 15h2.25a2.25 2.25 0 002.25-2.25v-1.372c0-.516-.351-.966-.852-1.091l-4.423-1.106c-.44-.11-.902.055-1.173.417l-.97 1.293c-.282.376-.769.542-1.21.38a12.035 12.035 0 01-7.143-7.143c-.162-.441.004-.928.38-1.21l1.293-.97c.363-.271.527-.734.417-1.173L6.963 3.102a1.125 1.125 0 00-1.091-.852H4.5A2.25 2.25 0 002.25 4.5v2.25z" />
            </svg>
          </span>
          <span class="text-sm">+91 789 299 4174</span>
        </a>

        <a
          href="https://www.linkedin.com/in/shruti-hegde-7b927a3aa"
          target="_blank"
          class="flex items-center gap-3 text-gray-600 hover:text-gray-900 transition-colors group"
        >
          <span class="flex items-center justify-center w-9 h-9 rounded-full border border-gray-200 text-gray-400 group-hover:border-gray-400 group-hover:text-gray-600 transition-all">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
              <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
            </svg>
          </span>
          <span class="text-sm">LinkedIn</span>
        </a>
        <a
          href="mailto:shrur.33@gmail.com"
          class="flex items-center gap-3 text-gray-600 hover:text-gray-900 transition-colors group"
        >
          <span class="flex items-center justify-center w-9 h-9 rounded-full border border-gray-200 text-gray-400 group-hover:border-gray-400 group-hover:text-gray-600 transition-all">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 01-2.25 2.25H4.5a2.25 2.25 0 01-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0019.5 4.5H4.5a2.25 2.25 0 00-2.25 2.25m19.5 0l-9.75 6.75L2.25 6.75" />
            </svg>
          </span>
          <span class="text-sm">shrur.33@gmail.com</span>
        </a>

        <div class="flex items-center gap-3 text-gray-600">
          <span class="flex items-center justify-center w-9 h-9 rounded-full border border-gray-200 text-gray-400">
            <svg xmlns="http://www.w3.org/2000/svg" class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
              <path stroke-linecap="round" stroke-linejoin="round" d="M15 10.5a3 3 0 11-6 0 3 3 0 016 0z" />
              <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 10.5c0 7.142-7.5 11.25-7.5 11.25S4.5 17.642 4.5 10.5a7.5 7.5 0 1115 0z" />
            </svg>
          </span>
          <span class="text-sm">Bengaluru, India</span>
        </div>
      </div>
    </div>
  </section>
  <footer class="footer">
    <div class="container footer-inner">
      <span class="mono">© 2026 Shruti Hegde</span>
      <span class="mono">Built with Vue</span>
    </div>
  </footer>
</template>

<style scoped>

.contact-inner {
  max-width: 760px;
  margin: 0 auto;
}

.section-label {
  font-family: 'DM Mono', monospace;
  font-size: 12px;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: #888;
  margin-bottom: 20px;
}

.contact-heading {
  font-family: 'DM Serif Display', serif;
  font-size: clamp(42px, 8vw, 68px);
  font-weight: 400;
  line-height: 1.05;
  margin: 0 0 8px;
}

.contact-heading em {
  font-style: italic;
  color: #888;
}

.footer {
  background-color: var(--rule);
  padding: 2rem 0;
}
.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.footer-inner .mono { font-size: 0.7rem; color: var(--muted); }

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.4; }
}

</style>