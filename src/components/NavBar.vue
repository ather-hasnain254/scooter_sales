<template>
  <nav class="sticky top-0 z-50 bg-[#1a1a2e] text-white shadow-lg">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo -->
        <div class="flex-shrink-0">
          <a href="#" class="text-lg font-bold tracking-wide text-white hover:text-red-400 transition-colors">
            Hawaiian Style Rentals & Sales
          </a>
        </div>

        <!-- Desktop Nav Links -->
        <div class="hidden lg:flex items-center space-x-1">
          <a v-for="link in navLinks" :key="link" href="#"
            class="px-3 py-2 text-xs font-semibold uppercase tracking-wider text-gray-300 hover:text-white hover:bg-white/10 rounded transition-colors">
            {{ link }}
          </a>
        </div>

        <!-- Search Icon + Hamburger -->
        <div class="flex items-center space-x-3">
          <button class="text-gray-300 hover:text-white transition-colors">
            <svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/>
            </svg>
          </button>
          <button @click="menuOpen = !menuOpen" class="lg:hidden text-gray-300 hover:text-white transition-colors">
            <svg v-if="!menuOpen" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
            </svg>
            <svg v-else class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="menuOpen" class="lg:hidden bg-[#16162a] border-t border-white/10">
      <div class="px-4 pt-2 pb-4 space-y-1">
        <a v-for="link in navLinks" :key="link" href="#"
          class="block px-3 py-2 text-sm font-semibold uppercase tracking-wider text-gray-300 hover:text-white hover:bg-white/10 rounded transition-colors">
          {{ link }}
        </a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)
const navLinks = ['SHOP', 'USED', 'NEW', 'ACCESSORIES', 'WARRANTY', 'DELIVERY', 'FINANCING', 'CART', 'NEWS']
</script>
