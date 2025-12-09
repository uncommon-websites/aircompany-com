<script lang="ts">
  export let image = "https://images.unsplash.com/photo-1565610212538-48b524792671?q=80&w=2070&auto=format&fit=crop";
</script>

<section class="relative h-screen w-full overflow-hidden">
  <!-- Background Image -->
  <div class="absolute inset-0">
    <img 
      src={image} 
      alt="Industrial Background" 
      class="w-full h-full object-cover"
    />
    <!-- Overlay to ensure text readability -->
    <div class="absolute inset-0 bg-black/20"></div>
  </div>

  <!-- Content -->
  <div class="relative z-10 h-full flex flex-col items-center justify-center text-center px-4">
    <h1 class="text-white text-5xl md:text-7xl font-medium tracking-tight mb-4">
      AIRMADE<sup class="text-2xl md:text-3xl relative top-[-0.5em]">™</sup> Technology
    </h1>
    <p class="text-white/90 text-lg md:text-xl font-light tracking-wide mb-8 max-w-2xl">
      An Advanced Carbon Conversion Technology Platform
    </p>
    <button class="px-6 py-2 rounded-full bg-white/20 backdrop-blur-md border border-white/20 text-white text-sm font-medium hover:bg-white/30 transition-all duration-300">
      Learn More
    </button>
  </div>
</section>
