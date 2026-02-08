<template>
  <section>
    <h2 class="section-title flex items-center gap-3">
      <span class="w-8 h-1 bg-amber-600 rounded-full"></span>
      Initiatives & Products
    </h2>
    <p class="section-subtitle">
      Ventures and platforms I’ve built across software, publishing, and education.
    </p>
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
      <div
        v-for="(initiative, i) in initiatives"
        :key="i"
        class="rounded-2xl p-6 bg-slate-800/90 border border-slate-700 hover:border-cyan-400/60 hover:shadow-xl transition-all duration-300 group flex flex-col h-full"
      >
        <div class="flex-1">
          <h3 class="text-xl font-bold mb-2 text-slate-100 group-hover:text-cyan-300 transition-colors">
            {{ initiative.title }}
          </h3>
          <p class="text-sm font-medium text-slate-400 mb-4 uppercase tracking-wider">
            {{ initiative.subtitle }}
          </p>
          <p class="text-slate-300 text-sm leading-relaxed mb-4">
            {{ initiative.note }}
          </p>
        </div>

        <a
          :href="initiative.url"
          target="_blank"
          rel="noreferrer"
          :aria-label="`Visit ${initiative.title}`"
          class="inline-flex items-center gap-2 text-sm font-semibold text-cyan-300 hover:gap-3 transition-all"
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
    title: "Homepage.lk",
    subtitle: "Sri Lankan Home Portal",
    url: "https://homepage.lk/",
    note: "News & blog syndication, poya/thithi calendar, weather, and daily essentials",
  },
  {
    title: "LankaPayslip",
    subtitle: "Payroll & Tax Compliance Suite",
    url: "https://lankapayslip.com/",
    note: "Automates APIT/PAYE, generates RAMIS-compliant PAYE files, and manages EPF/ETF",
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
