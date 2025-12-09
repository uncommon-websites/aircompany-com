<script lang="ts">
  export let image: string;
  export let title: string;
  export let subtitle: string = "";
  export let buttonText: string;
</script>

<div class="w-full max-w-[1400px] mx-auto px-4 md:px-6 py-12">
  <div class="relative w-full aspect-[16/9] md:aspect-[21/9] rounded-sm overflow-hidden group">
    <!-- Image -->
    <img 
      src={image} 
      alt={title.replace(/<[^>]*>/g, '')} 
      class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
    />
    
    <!-- Gradient Overlay -->
    <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent"></div>

    <!-- Content -->
    <div class="absolute bottom-0 left-0 p-8 md:p-12 w-full">
      <h2 class="text-white text-4xl md:text-5xl font-medium tracking-tight mb-2">
        {@html title}
      </h2>
      {#if subtitle}
        <p class="text-white/80 text-lg md:text-xl font-light mb-6">
          {subtitle}
        </p>
      {/if}
      <button class="px-6 py-2 mt-2 rounded-full bg-white/20 backdrop-blur-md border border-white/20 text-white text-sm font-medium hover:bg-white/30 transition-all duration-300">
        {buttonText}
      </button>
    </div>
  </div>
</div>
