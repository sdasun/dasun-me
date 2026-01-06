<template>
  <section>
    <h2 class="text-2xl font-bold mb-6 flex items-center gap-3">
      <span class="w-8 h-1 bg-purple-600 rounded-full"></span>
      Interests
    </h2>
    <div class="flex flex-wrap gap-3">
      <div
        v-for="(interest, idx) in interests"
        :key="idx"
        class="group flex items-center gap-2 px-4 py-2 rounded-full bg-gray-50 dark:bg-slate-800/50 border border-gray-100 dark:border-slate-700/50 hover:border-purple-200 dark:hover:border-purple-800 transition-colors duration-300"
      >
        <component 
          :is="interest.icon" 
          :size="16" 
          class="text-purple-600 dark:text-purple-400 group-hover:scale-110 transition-transform" 
        />
        <span class="text-sm font-medium text-gray-700 dark:text-gray-300">
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
