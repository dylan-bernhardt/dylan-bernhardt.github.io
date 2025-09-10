<template>
  <span
    class="w-fit bg-purple-100 text-purple-800 text-xs font-medium px-2.5 py-0.5 rounded-sm dark:bg-purple-900 dark:text-purple-300">
    {{ props.name }}
  </span>
</template>

<script setup lang="ts">
const props: { readonly name?: string } = defineProps(["name"]);
</script>
