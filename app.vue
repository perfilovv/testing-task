<template>
  <div class="flex flex-col min-h-screen items-center">
    <div class="w-[1200px] flex flex-col">
      <Header />
      <main class="flex-grow p-6">
        <NuxtPage />
      </main>
    </div>
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue';
</script>

