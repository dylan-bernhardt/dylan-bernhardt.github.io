<template>
  <div>
    <Header class="fixed top-6 left-[50%] -translate-x-[50%]" />
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
