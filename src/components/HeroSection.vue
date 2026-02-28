<template>
  <section class="relative h-screen min-h-[600px] flex items-center justify-center overflow-hidden">
    <!-- Background Image -->
    <img
      src="https://picsum.photos/seed/scooter1/1600/800"
      alt="Scooter Hero"
      class="absolute inset-0 w-full h-full object-cover"
    />
    <!-- Dark Overlay -->
    <div class="absolute inset-0 bg-black/50"></div>

    <!-- Content -->
    <div class="relative z-10 text-center px-4">
      <h1 class="text-5xl sm:text-7xl md:text-8xl font-bold text-white mb-8 drop-shadow-lg"
          style="font-family: 'Dancing Script', cursive;">
        Hawaii's New Favorite Moped
      </h1>
      <a href="#"
        class="inline-block bg-[#c41e3a] hover:bg-red-700 text-white font-bold uppercase tracking-widest px-10 py-4 text-sm transition-colors duration-200 shadow-lg">
        SHOP NEW OR USED
      </a>
    </div>
  </section>
</template>
