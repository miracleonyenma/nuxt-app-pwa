<!-- ./pages/index.vue -->
<script setup lang="ts">
const { $pwa } = useNuxtApp();

onMounted(() => {
  if ($pwa.offlineReady) {
    console.log("App ready to work offline");
  }
});
</script>
<template>
  <section>
    <h1>Hello there</h1>
  </section>
</template>
