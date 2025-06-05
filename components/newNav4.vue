
<template>
  <header class="bg-gray-800 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16 items-center">
        <!-- Logo -->
        <div class="flex-shrink-0 text-xl font-bold">TerriYates</div>

        <!-- Desktop Nav -->
        <nav class="hidden md:flex space-x-6">
          <NuxtLink to="/" class="hover:text-blue-500">Home</NuxtLink>
          <NuxtLink to="/photos" class="hover:text-blue-500">Photos</NuxtLink>
          <NuxtLink to="/video" class="hover:text-blue-500">Sound/Videos</NuxtLink>
          <NuxtLink to="/shows" class="hover:text-blue-500">Shows</NuxtLink>
          <NuxtLink to="/contact" class="hover:text-blue-500">Contact</NuxtLink>
        </nav>

        <!-- Mobile Hamburger -->
        <button
          @click="isOpen = !isOpen"
          class="md:hidden p-2 rounded hover:bg-gray-100 focus:outline-none"
        >
          <svg
            class="h-6 w-6"
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              :class="{ hidden: isOpen }"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-if="isOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="isOpen" class="md:hidden px-4 pb-4 space-y-2">
      <NuxtLink to="/" class="block hover:text-blue-500">Home</NuxtLink>
    <NuxtLink to="/photos" class="blockhover:text-blue-500">Photos</NuxtLink>
    <NuxtLink to="/video" class="block hover:text-blue-500">Sound/Videos</NuxtLink>
    <NuxtLink to="/shows" class="hover:text-blue-500">Shows</NuxtLink>
    <NuxtLink to="/contact" class="block hover:text-blue-500">Contact</NuxtLink>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';
const isOpen = ref(false);
</script>
