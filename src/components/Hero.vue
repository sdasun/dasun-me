<template>
  <div class="glass-card rounded-3xl p-8 md:p-12 relative overflow-hidden group">
    <!-- Animated Background Gradient -->
    <div
      class="absolute -top-24 -right-24 w-64 h-64 bg-blue-500/20 rounded-full blur-3xl group-hover:bg-blue-500/30 transition-colors duration-700"
    />
    <div
      class="absolute -bottom-24 -left-24 w-64 h-64 bg-purple-500/20 rounded-full blur-3xl group-hover:bg-purple-500/30 transition-colors duration-700"
    />

    <div class="relative z-10">
      <div class="flex flex-col md:flex-row gap-8 items-center md:items-start">
        <div class="flex-1 text-center md:text-left">
          <h1 class="text-5xl md:text-7xl font-bold tracking-tight mb-4">
            Dasun <span class="gradient-text">Sameera</span> Weerasinghe
          </h1>
          <h2 class="text-xl md:text-2xl font-medium text-gray-600 dark:text-gray-300 mb-6">
            Senior Software Engineer · Content Creator · Entrepreneur
            <span class="hidden md:inline mx-2 text-gray-300 dark:text-gray-700">|</span>
            <span class="block md:inline mt-1 md:mt-0">Building Long-Living Systems & Ideas</span>
          </h2>
          
<p class="text-lg text-gray-600 dark:text-gray-400 leading-relaxed max-w-2xl mx-auto md:mx-0 mb-8">
  Senior software engineer, content creator, and entrepreneur with over 20 years of experience.
  I build software systems, run podcasts and YouTube channels, and create businesses that live
  at the intersection of technology, thinking, and human meaning.
</p>


          <div class="flex flex-wrap justify-center md:justify-start gap-4">
            <a
              v-for="social in socialLinks"
              :key="social.name"
              :href="social.url"
              target="_blank"
              rel="noreferrer"
              class="p-3 rounded-2xl bg-white dark:bg-slate-800 shadow-sm hover:shadow-md hover:scale-110 hover:-translate-y-1 transition-all duration-300 border border-gray-100 dark:border-slate-700 group/icon"
            >
              <component 
                :is="social.icon" 
                :size="24" 
                class="text-gray-600 dark:text-gray-400 group-hover/icon:text-blue-600 dark:group-hover/icon:text-blue-400 transition-colors" 
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
