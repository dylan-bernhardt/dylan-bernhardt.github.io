<template>
  <div>
    <Header class="fixed top-0" />
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  title: "Portfolio",
  htmlAttrs: {
    class: "font-display dark",
  },
});
</script>
