<template>
  <div
    class="w-screen max-w-screen min-h-screen bg-white dark:bg-gray-950 pt-40 justify-center flex px-4">
    <div class="flex flex-col max-w-lg lg:max-w-5xl w-full gap-8">
      <span
        class="text-4xl font-extrabold text-gray-900 dark:text-gray-100 text-center">
        My projects
      </span>
      <div class="w-full h-fit columns-1 lg:columns-2 gap-4">
        <Project
          class="my-4 break-inside-avoid-column"
          v-for="project in projects"
          :project="project"></Project>
      </div>
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
