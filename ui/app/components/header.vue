<template>
  <nav class="fixed top-0 w-full bg-white/95 backdrop-blur-sm shadow-md z-50">
    <div class="container mx-auto px-6 py-4">
      <div class="flex items-center justify-between">
        <h1 class="text-2xl font-bold text-amber-800">Sejarah Islam</h1>
        <ul class="flex space-x-8">
          <li><a href="#hero" class="text-gray-700 hover:text-amber-600 transition-colors">Beranda</a></li>
          <li><a href="#eropa" class="text-gray-700 hover:text-amber-600 transition-colors">Eropa</a></li>
          <li><a href="#asia" class="text-gray-700 hover:text-amber-600 transition-colors">Asia</a></li>
          <li><a href="#timeline" class="text-gray-700 hover:text-amber-600 transition-colors">Timeline</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script setup>
// Smooth scroll behavior
onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({
          behavior: 'smooth',
          block: 'start'
        });
      }
    });
  });
});
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}
</style>