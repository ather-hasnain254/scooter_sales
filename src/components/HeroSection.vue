<template>
  <section class="relative h-screen min-h-[600px] flex items-center justify-center overflow-hidden">
    <!-- Gradient Background (replaces external photo) -->
    <div class="absolute inset-0"
         style="background: linear-gradient(135deg, #0f2027 0%, #203a43 40%, #2c5364 70%, #1a3a2a 100%);"></div>
    <!-- Decorative road-stripe overlay -->
    <div class="absolute inset-0 opacity-10"
         style="background-image: repeating-linear-gradient(90deg, transparent, transparent 48%, #fff 48%, #fff 52%);"></div>
    <!-- Dark Overlay -->
    <div class="absolute inset-0 bg-black/40"></div>

    <!-- Content -->
    <div class="relative z-10 text-center px-4">
      <h1 class="script-font text-5xl sm:text-7xl md:text-8xl font-bold text-white mb-8 drop-shadow-lg"
          style="font-family: 'Dancing Script', 'Pacifico', 'Brush Script MT', cursive; text-shadow: 2px 4px 12px rgba(0,0,0,0.7);">
        Hawaii's New Favorite Moped
      </h1>
      <a href="#"
        class="inline-block bg-[#c41e3a] hover:bg-red-700 text-white font-bold uppercase tracking-widest px-10 py-4 text-sm transition-colors duration-200 shadow-lg">
        SHOP NEW OR USED
      </a>
    </div>
  </section>
</template>
