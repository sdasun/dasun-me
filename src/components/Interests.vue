<template>
  <section>
    <h2 class="section-title flex items-center gap-3">
      <span class="w-8 h-1 bg-emerald-600 rounded-full"></span>
      Interests
    </h2>
    <p class="section-subtitle">
      Domains that shape how I think, build, and communicate.
    </p>
    <div class="flex flex-wrap gap-3">
      <div
        v-for="(interest, idx) in interests"
        :key="idx"
        class="group flex items-center gap-2 px-4 py-2 rounded-full bg-slate-800 border border-slate-700 hover:border-emerald-400/60 transition-colors duration-300"
      >
        <component 
          :is="interest.icon" 
          :size="16" 
          class="text-emerald-600 group-hover:scale-110 transition-transform" 
        />
        <span class="text-sm font-medium text-slate-200">
          {{ interest.name }}
        </span>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import {
  Book,
  Sparkles,
  Wand2,
  Compass,
  Code,
} from "lucide-vue-next";

const interests = [
  { name: "Literature", icon: Book },
  { name: "Astrology & Astronomy", icon: Sparkles },
  { name: "Magic & Symbolism", icon: Wand2 },
  { name: "Software Craftsmanship", icon: Code },
  { name: "Buddhism & Philosophy", icon: Compass },
];
</script>
