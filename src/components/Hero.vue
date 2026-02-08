<template>
  <div class="glass-card rounded-3xl p-7 md:p-11 relative overflow-hidden group">
    <!-- Animated Background Gradient -->
    <div
      class="absolute -top-24 -right-24 w-64 h-64 bg-cyan-500/25 rounded-full blur-3xl group-hover:bg-cyan-500/35 transition-colors duration-700"
    />
    <div
      class="absolute -bottom-24 -left-24 w-64 h-64 bg-emerald-500/20 rounded-full blur-3xl group-hover:bg-emerald-500/30 transition-colors duration-700"
    />

    <div class="relative z-10">
      <div class="flex flex-col md:flex-row gap-8 items-center md:items-start">
        <div class="flex-1 text-center md:text-left">
          <p class="inline-flex items-center rounded-full bg-cyan-500/10 border border-cyan-400/30 text-cyan-300 px-3 py-1 text-xs font-semibold tracking-wide mb-5">
            Senior Software Engineer
          </p>
          <h1 class="text-4xl md:text-6xl font-bold tracking-tight mb-4 text-slate-100">
            Dasun <span class="gradient-text">Sameera</span> Weerasinghe
          </h1>
          <h2 class="text-lg md:text-2xl font-medium text-slate-300 mb-5">
            Senior Software Engineer · Content Creator · Entrepreneur
            <span class="hidden md:inline mx-2 text-slate-600">|</span>
            <span class="block md:inline mt-1 md:mt-0">Building Long-Living Systems & Ideas</span>
          </h2>
          
          <p class="text-base md:text-lg text-slate-400 leading-relaxed max-w-2xl mx-auto md:mx-0 mb-8">
            Senior software engineer, content creator, and entrepreneur with over 20 years of experience.
            I build software systems, run podcasts and YouTube channels, and create businesses that live
            at the intersection of technology, thinking, and human meaning.
          </p>

          <div class="flex flex-wrap justify-center md:justify-start gap-3 mb-8">
            <a
              href="https://blog.dasun.me/"
              target="_blank"
              rel="noreferrer"
              class="inline-flex items-center rounded-xl bg-cyan-500 text-slate-950 px-4 py-2.5 text-sm font-semibold hover:bg-cyan-400 transition-colors"
            >
              Read Articles
            </a>
            <a
              href="https://www.linkedin.com/in/dasunsameera/"
              target="_blank"
              rel="noreferrer"
              class="inline-flex items-center rounded-xl bg-slate-800 border border-slate-700 text-slate-200 px-4 py-2.5 text-sm font-semibold hover:border-cyan-400/60 hover:text-cyan-300 transition-colors"
            >
              Connect on LinkedIn
            </a>
          </div>

          <div class="flex flex-wrap justify-center md:justify-start gap-4">
            <a
              v-for="social in socialLinks"
              :key="social.name"
              :href="social.url"
              target="_blank"
              rel="noreferrer"
              :aria-label="`Open ${social.name}`"
              class="p-3 rounded-2xl bg-slate-800/95 shadow-sm hover:shadow-md hover:scale-110 hover:-translate-y-1 transition-all duration-300 border border-slate-700 group/icon"
            >
              <component 
                :is="social.icon" 
                :size="24" 
                class="text-slate-300 group-hover/icon:text-cyan-300 transition-colors" 
              />
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import {
  Linkedin,
  Globe,
  Github,
  Twitter,
  Facebook,
  Youtube,
} from "lucide-vue-next";

const socialLinks = [
  {
    name: "LinkedIn",
    url: "https://www.linkedin.com/in/dasunsameera/",
    icon: Linkedin,
  },
  { name: "Blog", url: "https://blog.dasun.me/", icon: Globe },
  { name: "GitHub", url: "https://github.com/sdasun", icon: Github },
  { name: "Twitter", url: "https://twitter.com/d_dasun", icon: Twitter },
  { name: "Facebook", url: "https://www.facebook.com/dasun", icon: Facebook },
  { name: "YouTube", url: "https://www.youtube.com/", icon: Youtube },
];
</script>
