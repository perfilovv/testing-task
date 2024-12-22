<template>
  <header>
    <div class="bg-[#E0E3EE] p-4 rounded-b-[10px]"></div>
    <nav class="flex justify-end mt-5">
      <NuxtLink
        v-for="item in navItems"
        :key="item.path"
        :to="item.path"
        class="flex flex-col items-center rounded-md p-2 w-[86px] gap-1 cursor-pointer hover:underline"
        :class="{ 'bg-[#F4F5F9]': $route.path === item.path }"
      >
        <img :src="item.icon" :alt="item.label" class="w-5 h-5" />
        <span class="text-primary text-xs">{{ item.label }}</span>
      </NuxtLink>
    </nav>
  </header>
</template>

<script setup lang="ts">
const navItems = [
  { label: 'Избранное', path: '/favorites', icon: '/icons/favorite.svg' },
  { label: 'Склад', path: '/', icon: '/icons/warehouse.svg' },
  { label: 'Сделки', path: '/deals', icon: '/icons/deals.svg' },
];
</script>

