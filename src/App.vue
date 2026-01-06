<template>
  <div class="min-h-screen bg-gray-50 dark:bg-slate-950 transition-colors selection:bg-blue-500/30 selection:text-blue-600">
    <div class="max-w-7xl mx-auto px-4 py-8 sm:px-6 lg:px-8">
      
      <main class="space-y-16 md:space-y-24">
        <!-- Hero Section -->
        <Hero />
        
        <!-- Tech Stack -->
        <TechStack />
        
        <!-- Interests -->
        <Interests />
        
        <!-- Initiatives -->
        <Initiatives />
        
        <!-- Timeline -->
        <Timeline />
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
import Timeline from './components/Timeline.vue';
import Footer from './components/Footer.vue';
</script>
