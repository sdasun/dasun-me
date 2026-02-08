<template>
  <section>
    <h2 class="section-title flex items-center gap-3">
      <span class="w-8 h-1 bg-cyan-600 rounded-full"></span>
      Technical Stack
    </h2>
    <p class="section-subtitle">
      Core technologies I use to ship stable systems and product features at scale.
    </p>
    
    <div class="grid md:grid-cols-2 gap-x-10 gap-y-8">
      <div 
        v-for="(category, idx) in categories" 
        :key="idx"
      >
        <h3 class="text-sm font-semibold uppercase tracking-wider mb-3 text-slate-400">
          {{ category.title }}
        </h3>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in category.skills"
            :key="skill"
            class="px-3 py-1 rounded-lg text-sm bg-slate-800 text-slate-200 hover:bg-cyan-500/15 hover:text-cyan-300 transition-colors cursor-default"
          >
            {{ skill }}
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const categories = [
  {
    title: "Languages",
    skills: ["Python", "TypeScript", "JavaScript", "C#", "PHP", "Go", "C++"],
  },
  {
    title: "Frameworks & Runtimes",
    skills: [
      "Django",
      "FastAPI",
      "Vue.js",
      "Angular",
      "Node.js",
      "Laravel",
      "Next.js",
      "Nuxt.js",
      ".NET Core",
    ],
  },
  {
    title: "Cloud & Infrastructure",
    skills: ["AWS", "Pulumi", "Docker"],
  },
  {
    title: "Data & APIs",
    skills: [
      "PostgreSQL",
      "MySQL",
      "MongoDB",
      "DynamoDB",
      "Memcached",
      "Redis",
      "Couchbase",
      "Elasticsearch",
      "GraphQL",
    ],
  },
];
</script>
