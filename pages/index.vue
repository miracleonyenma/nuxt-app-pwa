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
  <section class="site-section">
    <div class="wrapper">
      <h1>Hello there</h1>
    </div>
  </section>
</template>
