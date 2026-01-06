<template>
  <section>
    <h2 class="text-3xl font-bold mb-8 flex items-center gap-3">
      <span class="w-8 h-1 bg-pink-600 rounded-full"></span>
      Initiatives & Products
    </h2>
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="(initiative, i) in initiatives"
        :key="i"
        class="glass-card rounded-2xl p-6 hover:shadow-2xl transition-all duration-300 group flex flex-col h-full"
      >
        <div class="flex-1">
          <h3 class="text-xl font-bold mb-2 group-hover:text-blue-600 dark:group-hover:text-blue-400 transition-colors">
            {{ initiative.title }}
          </h3>
          <p class="text-sm font-medium text-gray-500 dark:text-gray-400 mb-4 uppercase tracking-wider">
            {{ initiative.subtitle }}
          </p>
          <p class="text-gray-600 dark:text-gray-300 text-sm leading-relaxed mb-4">
            {{ initiative.note }}
          </p>
        </div>

        <a
          :href="initiative.url"
          target="_blank"
          rel="noreferrer"
          class="inline-flex items-center gap-2 text-sm font-semibold text-blue-600 dark:text-blue-400 hover:gap-3 transition-all"
        >
          Visit Product
          <ExternalLink :size="16" />
        </a>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ExternalLink } from "lucide-vue-next";

const initiatives = [
  {
    title: "Sigma Digital (Pvt) Ltd",
    subtitle: "Software & Product Company",
    url: "https://sigmadigital.net/",
    note: "Co‑Founder & Director · Since 2006",
  },
  {
    title: "Grantha.lk",
    subtitle: "Online Bookstore",
    url: "https://www.grantha.lk/",
    note: "Founder · Runs under Sigma Digital (Pvt) Ltd",
  },
  {
    title: "Grantha (Pvt) Ltd",
    subtitle: "Publishing Company",
    url: "https://www.grantha.lk/",
    note: "Co‑Founder & Director",
  },
  {
    title: "Tharu Kirana",
    subtitle: "Astrology Software",
    url: "https://www.tharukirana.com/",
    note: "Developed since 2006 · Used by professional astrologers",
  },
  {
    title: "Kendare.com",
    subtitle: "Web‑based Astrology Application",
    url: "https://www.kendare.com/",
    note: "Modern web version of Tharu Kirana",
  },
  {
    title: "Code With Dasun",
    subtitle: "YouTube Channel",
    url: "https://www.youtube.com/",
    note: "Coding, architecture & engineering thinking",
  },
  {
    title: "Dasun Sameera Weerasinghe",
    subtitle: "Personal YouTube",
    url: "https://www.youtube.com/",
    note: "Here I talk anything that interests me",
  },
];
</script>
