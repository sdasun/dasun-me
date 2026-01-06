<template>
  <section class="max-w-4xl mx-auto">
    <h2 class="text-3xl font-bold mb-12 flex items-center justify-center gap-3">
      <span class="w-8 h-1 bg-green-600 rounded-full"></span>
      Journey & Timeline
      <span class="w-8 h-1 bg-green-600 rounded-full"></span>
    </h2>

    <div class="relative space-y-8 before:absolute before:inset-0 before:ml-5 before:-translate-x-px md:before:ml-[50%] md:before:-translate-x-0.5 before:h-full before:w-0.5 before:bg-gray-200 dark:before:bg-gray-800 before:z-0">
      <div 
        v-for="(item, i) in timeline" 
        :key="i"
        class="relative flex items-center justify-between md:justify-normal md:odd:flex-row-reverse group is-active"
      >
        <!-- Icon/Dot -->
        <div class="absolute left-0 w-10 h-10 flex items-center justify-center bg-white dark:bg-slate-900 border-4 border-gray-100 dark:border-slate-800 rounded-full shadow shrink-0 md:order-1 md:group-odd:-translate-x-1/2 md:group-even:translate-x-1/2 z-10 md:left-1/2">
           <div class="w-3 h-3 bg-blue-600 rounded-full group-hover:scale-125 transition-transform"></div>
        </div>

        <!-- Content -->
        <div class="ml-16 md:ml-0 glass-card p-6 rounded-xl w-full md:w-[calc(50%-2.5rem)] hover:border-blue-500/30 transition-all shadow-lg hover:shadow-xl">
          <span class="inline-block px-3 py-1 mb-2 text-xs font-semibold tracking-wider text-blue-600 uppercase bg-blue-100 dark:bg-blue-900/30 rounded-full">
            {{ item.period }}
          </span>
          <h4 class="text-lg font-bold text-gray-900 dark:text-white mb-1">
            {{ item.title }}
          </h4>
          <p class="text-md font-medium text-gray-700 dark:text-gray-300 mb-2">
            {{ item.role }}
          </p>
          <p class="text-sm text-gray-500 dark:text-gray-400 leading-relaxed">
             {{ item.description || '' }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const timeline = [
  {
    title: "Fiberunlimited (NL) / Gapstars (NL)",
    role: "Senior Tech Lead",
    period: "2025 (May) – Present",
    description: "Leading the engineering team for Fiberunlimited",
  },
  {
    title: "Stekz / Gapstars (NL)",
    role: "Senior Tech Lead",
    period: "2021 – 2025 (April)",
    description: "Python+Vue centric DDD systems for EU clients",
  },
  {
    title: "Grantha (Pvt) Ltd", 
    role: "Co‑Founder", 
    period: "2017 – Present",
    description: "Building the digital publishing ecosystem of Sri Lanka"
  },
  {
    title: "Sigma Digital (Pvt) Ltd",
    role: "Co‑Founder & Director",
    period: "2014 – Present",
    description: "Driving product innovation and technical strategy."
  },
  {
    title: "IronOne Technologies",
    role: "Senior Tech Lead",
    period: "2010 – 2021",
    description: "Large‑scale mobile backends, cloud migration, mentoring teams",
  },
  {
    title: "University of Colombo School of Computing",
    role: "BIT Undergraduate",
    period: "2006 – 2011",
    description: "Foundation in Computer Science"
  },
  {
    title: "Sigma Digital",
    role: "Founder (Sole Proprietor)",
    period: "2006 – 2014",
    description: "Freelance web development and software services"
  },
  {
    title: "Vectronics R&D (Pvt) Ltd",
    role: "Software Developer",
    period: "2004 – 2006",
    description: "Educational & interactive learning software (Flash / ActionScript)",
  },
  {
    title: "Isipathana College, Colombo",
    role: "Student",
    period: "1991 – 2004",
    description: "Primary and Secondary Education"
  },
];
</script>
