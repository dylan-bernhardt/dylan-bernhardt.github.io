<template>
  <div>
    <div class="w-full p-4 fixed flex items-center justify-center z-50 top-6">
      <Header class="" />
    </div>
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  title: "Dylan Bernhardt",
  htmlAttrs: {
    class: "font-display dark",
  },
});
</script>
