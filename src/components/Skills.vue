<template>
  <section id="skills" class="skills py-30 ">
    <div class="container">
        <header class="section-header mb-10">
            <p class="section-label mono">04 / Skills</p>
            <h2 class="section-title">Technical<br/><em>Skills</em></h2>
        </header>
        <!-- Grid -->
        <div class="max-w-6xl mx-auto grid md:grid-cols-3 gap-6">
            <div
                v-for="skill in skills"
                :key="skill.title"
                class="bg-[#f4f1eb] p-6 rounded-xl hover:shadow-lg transition"
            >
                <!-- Title -->
                <div class="flex items-center gap-2 mb-4">
                    <span>{{ skill.icon }}</span>
                    <h3 class="font-semibold text-lg">{{ skill.title }}</h3>
                </div>

                <!-- Tags -->
                <div class="flex flex-wrap gap-2">
                    <span
                        v-for="item in skill.items"
                        :key="item"
                        class="px-3 py-1 text-sm rounded-full bg-black text-gray-300"
                    >
                        {{ item }}
                    </span>
                </div>

            </div>
        </div>
    </div>
  </section>
</template>
<script setup>
const skills = [
  {
    title: "Frontend Technologies",
    icon: "💻",
    items: ["Vue.js", "JavaScript", "HTML5", "CSS3", "jQuery"],
  },
  {
    title: "Frameworks",
    icon: "⚙️",
    items: ["Laravel", "Bootstrap", "Tailwind CSS"],
  },
  {
    title: "Tools",
    icon: "🛠️",
    items: ["Git", "GitHub", "ddev"],
  },
  {
    title: "Backend",
    icon: "🗄️",
    items: ["PHP", "Laravel", "MySQL"],
  },
  {
    title: "CMS",
    icon: "🌐",
    items: ["TYPO3"],
  },
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