<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="w-full bg-white shadow-sm mb-5">
    <div class="wrapper">
      <nav class="flex justify-center gap-5 py-4 text-sm font-medium text-gray-700">
        <RouterLink to="/" class="hover:text-[#FF5F5F] transition-colors">Home</RouterLink>
        <RouterLink to="/about" class="hover:text-[#FF5F5F] transition-colors">About</RouterLink>
        <RouterLink to="/contact" class="hover:text-[#FF5F5F] transition-colors">Contact</RouterLink>
        <RouterLink to="/intro" class="hover:text-[#FF5F5F] transition-colors">Intro</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

