<template>
  <button @click="toggleTheme()" class="bg-gray-300">changer theme</button>
</template>

<script setup>
let isDarkModeEnabled = true;
function toggleTheme() {
  isDarkModeEnabled = !isDarkModeEnabled;
  document.documentElement.classList.toggle("dark", isDarkModeEnabled);
}
</script>
