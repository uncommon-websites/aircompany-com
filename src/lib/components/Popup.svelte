<script lang="ts">
  let visible = true;
</script>

{#if visible}
  <div class="fixed bottom-6 right-6 z-50 bg-white shadow-lg border border-gray-100 p-6 max-w-sm flex items-start gap-4 animate-in slide-in-from-bottom-4 duration-500">
    <div class="flex-1">
      <p class="text-sm font-medium text-black leading-snug">
        Be the first to know<br>AIRCO's next steps
      </p>
    </div>
    <button 
      on:click={() => visible = false}
      class="text-gray-400 hover:text-black transition-colors"
      aria-label="Close"
    >
      <svg width="12" height="12" viewBox="0 0 12 12" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M1 1L11 11M1 11L11 1" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/>
      </svg>
    </button>
  </div>
{/if}
