<template>
  <div class="page-bg min-h-screen transition-colors selection:bg-cyan-500/25 selection:text-cyan-900">
    <div class="max-w-6xl mx-auto px-4 py-6 sm:px-6 md:py-10 lg:px-8">
      <header class="glass-card rounded-2xl px-4 py-3 md:px-6 md:py-4 mb-8 sticky top-4 z-20 reveal-section">
        <nav class="flex flex-col gap-3 md:flex-row md:items-center md:justify-between">
          <a
            href="#top"
            class="font-display text-base md:text-lg font-semibold tracking-tight text-slate-100"
          >
            dasun.me
          </a>
          <div class="flex flex-wrap gap-2 md:gap-3">
            <a
              v-for="item in navItems"
              :key="item.href"
              :href="item.href"
              class="nav-chip"
            >
              {{ item.label }}
            </a>
          </div>
        </nav>
      </header>

      <main class="space-y-14 md:space-y-18" id="top">
        <section id="about" class="reveal-section reveal-delay-1">
          <Hero />
        </section>

        <section id="stack" class="section-shell reveal-section reveal-delay-2">
          <TechStack />
        </section>

        <section id="interests" class="section-shell reveal-section reveal-delay-3">
          <Interests />
        </section>

        <section id="work" class="section-shell reveal-section reveal-delay-4">
          <Initiatives />
        </section>

        <section id="projects" class="section-shell reveal-section reveal-delay-5">
          <Projects />
        </section>

        <section id="journey" class="section-shell reveal-section reveal-delay-6">
          <Timeline />
        </section>
      </main>

      <Footer />
    </div>
  </div>
</template>

<script setup lang="ts">
import Hero from './components/Hero.vue';
import TechStack from './components/TechStack.vue';
import Interests from './components/Interests.vue';
import Initiatives from './components/Initiatives.vue';
import Projects from './components/Projects.vue';
import Timeline from './components/Timeline.vue';
import Footer from './components/Footer.vue';

const navItems = [
  { href: '#about', label: 'About' },
  { href: '#stack', label: 'Tech Stack' },
  { href: '#interests', label: 'Interests' },
  { href: '#work', label: 'Products' },
  { href: '#projects', label: 'Projects' },
  { href: '#journey', label: 'Timeline' },
];
</script>
