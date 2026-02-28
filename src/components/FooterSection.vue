<template>
  <footer class="bg-[#12122a] text-gray-400">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-14">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-10">
        <!-- SHOP -->
        <div>
          <h3 class="text-white font-extrabold uppercase tracking-widest text-sm mb-4">SHOP</h3>
          <ul class="space-y-2">
            <li v-for="item in shopLinks" :key="item">
              <a href="#" class="hover:text-white text-sm transition-colors">{{ item }}</a>
            </li>
          </ul>
        </div>
        <!-- CUSTOMER SERVICE -->
        <div>
          <h3 class="text-white font-extrabold uppercase tracking-widest text-sm mb-4">Customer Service</h3>
          <ul class="space-y-2">
            <li v-for="item in serviceLinks" :key="item">
              <a href="#" class="hover:text-white text-sm transition-colors">{{ item }}</a>
            </li>
          </ul>
        </div>
        <!-- MANUALS -->
        <div>
          <h3 class="text-white font-extrabold uppercase tracking-widest text-sm mb-4">Manuals</h3>
          <ul class="space-y-2">
            <li v-for="item in manualLinks" :key="item">
              <a href="#" class="hover:text-white text-sm transition-colors">{{ item }}</a>
            </li>
          </ul>
        </div>
        <!-- CONTACT -->
        <div>
          <h3 class="text-white font-extrabold uppercase tracking-widest text-sm mb-4">Contact</h3>
          <ul class="space-y-2 text-sm">
            <li>1234 Aloha Ave</li>
            <li>Honolulu, HI 96813</li>
            <li>
              <a href="tel:8085551234" class="hover:text-white transition-colors">Phone: (808) 555-1234</a>
            </li>
            <li>
              <a href="mailto:info@hawaiianscooters.com" class="hover:text-white transition-colors">info@hawaiianscooters.com</a>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <!-- Bottom Bar -->
    <div class="border-t border-white/10 py-5">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-3 text-xs text-gray-500">
        <span>&copy; {{ new Date().getFullYear() }} Hawaiian Style Rentals & Sales. All rights reserved.</span>
        <a href="#" class="hover:text-white transition-colors">Back to top ↑</a>
      </div>
    </div>
  </footer>
</template>

<script setup>
const shopLinks = ['Buddy', 'Roughhouse', 'Hooligan', 'Blur', 'Black Cat']
const serviceLinks = ['Test Ride', 'Delivery', 'Financing', 'Warranty', 'Repair Service']
const manualLinks = ['Genuine Manuals', 'Maintenance', 'Parts']
</script>
