<template>
  <section>
    <h2 class="section-title flex items-center gap-3">
      <span class="w-8 h-1 bg-violet-500 rounded-full"></span>
      Projects
    </h2>
    <p class="section-subtitle">
      Open source work and legacy products that shaped my engineering journey.
    </p>

    <div class="mb-10">
      <h3
        class="text-sm font-semibold uppercase tracking-wider mb-4 text-slate-400"
      >
        Open Source Projects
      </h3>
      <div class="grid md:grid-cols-2 gap-5">
        <article
          v-for="project in openSourceProjects"
          :key="project.title"
          class="rounded-2xl p-5 bg-slate-800/90 border border-slate-700 hover:border-cyan-400/60 transition-colors"
        >
          <h4 class="text-lg font-bold text-slate-100 mb-2">
            {{ project.title }}
          </h4>
          <p class="text-sm text-slate-300 leading-relaxed mb-4">
            {{ project.description }}
          </p>
          <div class="flex flex-wrap gap-3">
            <a
              :href="project.repoUrl"
              target="_blank"
              rel="noreferrer"
              :aria-label="`Open repository for ${project.title}`"
              class="inline-flex items-center gap-2 text-sm font-semibold text-cyan-300"
            >
              <Github :size="15" />
              Source
            </a>
            <a
              v-if="project.liveUrl"
              :href="project.liveUrl"
              target="_blank"
              rel="noreferrer"
              :aria-label="`Open demo for ${project.title}`"
              class="inline-flex items-center gap-2 text-sm font-semibold text-emerald-300"
            >
              <ExternalLink :size="15" />
              Live
            </a>
          </div>
        </article>
      </div>
    </div>

    <div>
      <h3
        class="text-sm font-semibold uppercase tracking-wider mb-4 text-slate-400"
      >
        Discontinued Projects
      </h3>
      <div class="grid md:grid-cols-3 gap-4">
        <article
          v-for="project in discontinuedProjects"
          :key="project.title"
          class="rounded-xl p-4 bg-slate-900/80 border border-slate-800"
        >
          <h4 class="text-sm font-semibold text-slate-200 mb-2">
            {{ project.title }}
          </h4>
          <p class="text-xs text-slate-400 leading-relaxed">
            {{ project.description }}
          </p>
        </article>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ExternalLink, Github } from "lucide-vue-next";

const openSourceProjects = [
  {
    title: "keyTouch",
    description: "Open source Sinhala typing software for Windows.",
    repoUrl: "https://github.com/sdasun/KeyTouch",
    liveUrl: "",
  },
  {
    title: "indic-transliterator",
    description:
      "Indic language transliterator for Sinhala, Devanagari, Tamil, and ISO15919 (phonetic).",
    repoUrl: "https://github.com/sdasun/indic-transliterator",
    liveUrl: "",
  },
  {
    title: "Moon Phase / Naming Simulator",
    description: "Explores how nakshatra influences moon-month naming.",
    repoUrl: "https://github.com/sdasun/nakshatra",
    liveUrl: "https://moon.tharukirana.com/",
  },
  {
    title: "Mac Wijesekara",
    description: "Sinhala Wijesekara keyboard layout for macOS.",
    repoUrl: "https://github.com/sdasun/mac-wijesekara",
    liveUrl: "",
  },
];

const discontinuedProjects = [
  {
    title: "Educational Video CD (2006 - 2009)",
    description:
      "Digital learning content for FL Studio, Reason, Flash, Photoshop, and Inkscape.",
  },
  {
    title: "cPlus (2010 January - 2010 June)",
    description:
      "Digital magazine distributed as CD and printed media at the same time.",
  },
  {
    title: "SinhalaWordPad (2006)",
    description: "Legacy none Unicode typing software.",
  },
];
</script>
