<template></template>

<script setup lang="ts">
const projects = ref([]);

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
