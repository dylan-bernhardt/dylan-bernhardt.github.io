<template>
  <span
    class="w-fit bg-neutral-200 dark:bg-neutral-700 text-neutral-900 dark:text-neutral-100 text-sm font-medium px-3 py-1 rounded-md text-nowrap">
    {{ props.name }}
  </span>
</template>

<script setup lang="ts">
const props: { readonly name?: string } = defineProps(["name"]);
</script>
