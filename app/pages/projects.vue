<template>
  <div
    class="bg-neutral-200 dark:bg-black min-h-screen w-full max-w-screen flex flex-col items-center overflow-hidden px-8 sm:px-4">
    <span class="dark:text-white mt-44 mb-12 text-6xl font-bold">
      My projects
    </span>
    <div class="w-full max-w-4xl h-fit grid grid-cols-1 lg:grid-cols-2 gap-4">
      <Project v-for="project in projects" :project="project"></Project>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Project {
  title: string;
  techs: string[];
  description: string;
  tasks: string[];
  githubLink: string;
}

const projects: Ref<Project[]> = ref([]);

onMounted(async () => {
  try {
    const res = await fetch("/projects.json");
    if (!res.ok) throw new Error("Erreur lors du chargement du fichier JSON.");
    projects.value = await res.json();
    console.log(projects.value);
  } catch (error) {
    console.error(error);
  }
});
</script>
