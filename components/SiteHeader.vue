<template>
  <header class="site-header">
    <div class="wrapper">
      <SiteLogo />
      <SiteNav />
    </div>
  </header>
</template>
<style scoped>
.site-header {
  @apply bg-white p-4 sticky top-0 z-10;
}

.site-header > .wrapper {
  @apply flex items-center justify-between max-w-6xl mx-auto;
}
</style>
