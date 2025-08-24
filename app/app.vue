<template>
  <div>
    <Header class="fixed top-4 left-1/2 transform -translate-x-1/2" />
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  htmlAttrs: {
    class: "font-display dark",
  },
});
</script>
