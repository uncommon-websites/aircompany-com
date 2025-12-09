<script lang="ts">
  import Header from "$lib/components/Header.svelte";
  import Hero from "$lib/components/Hero.svelte";
  import FeatureCard from "$lib/components/FeatureCard.svelte";
  import BlogSection from "$lib/components/BlogSection.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import Popup from "$lib/components/Popup.svelte";
</script>

<main class="w-full bg-white">
  <Header />
  
  <Hero />
  
  <div class="space-y-4 md:space-y-8 py-4 md:py-8">
    <FeatureCard 
      image="https://images.unsplash.com/photo-1483304528321-0674f0040030?q=80&w=2070&auto=format&fit=crop"
      title="AIRMADE<sup class='text-2xl md:text-3xl relative top-[-0.5em]'>®</sup> SAF"
      subtitle="Fully-Formulated Jet Fuel Made from CO₂"
      buttonText="Learn More"
    />
    
    <FeatureCard 
      image="https://images.unsplash.com/photo-1551288049-bebda4e38f71?q=80&w=2070&auto=format&fit=crop"
      title="Advancing the Future of Fuel"
      buttonText="Technology for Government & Defense"
    />
  </div>

  <BlogSection />
  
  <Footer />
  
  <Popup />
</main>

