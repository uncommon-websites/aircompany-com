<script lang="ts">
  const posts = [
    {
      image: "https://images.unsplash.com/photo-1614728853913-1e32005e307a?q=80&w=2070&auto=format&fit=crop",
      badge: { text: "AIR&D", color: "bg-[#FF4D00]" },
      title: "AIRMADE™ on Mars: Visualizing the Future of Fuel Beyond Earth",
      date: "November 18, 2025"
    },
    {
      image: "https://images.unsplash.com/photo-1581093458891-8f3086c85e53?q=80&w=2070&auto=format&fit=crop",
      badge: { text: "AIR&D", color: "bg-[#004DFF]" },
      title: "AIR&D Case Study 001: AIRMADE® Rocket Fuel",
      date: "November 14, 2025"
    },
    {
      image: "https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=2064&auto=format&fit=crop",
      badge: null, // This image seems to have the text embedded or is a special case
      title: "AIR&D: AIRCO's Internal Research & Development Engine",
      date: "November 13, 2025"
    }
  ];
</script>

<section class="w-full max-w-[1400px] mx-auto px-4 md:px-6 py-20">
  <!-- Header -->
  <div class="flex justify-between items-end mb-12">
    <h2 class="text-4xl md:text-5xl font-normal tracking-tight text-black">
      Blog: AIR.Index
    </h2>
    <a href="#" class="flex items-center gap-2 text-sm font-medium hover:opacity-70 transition-opacity">
      <span class="w-2 h-2 rounded-full bg-blue-600"></span>
      See All
    </a>
  </div>

  <!-- Grid -->
  <div class="grid grid-cols-1 md:grid-cols-3 gap-x-6 gap-y-12">
    {#each posts as post}
      <div class="group cursor-pointer">
        <!-- Image Container -->
        <div class="relative aspect-[4/5] w-full overflow-hidden bg-gray-100 mb-6">
          <img 
            src={post.image} 
            alt={post.title} 
            class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105"
          />
          
          {#if post.badge}
            <div class="absolute top-4 right-4 w-16 h-20 {post.badge.color} flex items-center justify-center">
              <span class="text-white font-bold tracking-widest -rotate-90 text-xs whitespace-nowrap">
                {post.badge.text}
              </span>
            </div>
          {/if}
          
          <!-- Special case for the 3rd card which looks like it has a logo in the center -->
          {#if !post.badge}
             <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
                <span class="text-white/50 text-4xl font-bold tracking-tighter">AIR&D</span>
             </div>
          {/if}
        </div>

        <!-- Content -->
        <h3 class="text-lg font-medium leading-snug mb-2 pr-4">
          {post.title}
        </h3>
        <p class="text-xs text-gray-400 uppercase tracking-wide">
          {post.date}
        </p>
      </div>
    {/each}
  </div>
</section>
