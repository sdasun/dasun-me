<template>
  <section>
    <h2 class="text-2xl font-bold mb-6 flex items-center gap-3">
      <span class="w-8 h-1 bg-blue-600 rounded-full"></span>
      Technical Stack
    </h2>
    
    <div class="grid md:grid-cols-2 gap-x-12 gap-y-8">
      <div 
        v-for="(category, idx) in categories" 
        :key="idx"
      >
        <h3 class="text-sm font-medium uppercase tracking-wider mb-3 text-gray-500 dark:text-gray-400">
          {{ category.title }}
        </h3>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in category.skills"
            :key="skill"
            class="px-3 py-1 rounded-md text-sm bg-gray-100 dark:bg-slate-800 text-gray-700 dark:text-gray-300 hover:bg-blue-50 dark:hover:bg-blue-900/20 hover:text-blue-600 dark:hover:text-blue-400 transition-colors cursor-default"
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
