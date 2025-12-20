<script lang="ts">
  export let name: string;
  export let date: string;
  export let url: string;
  export let role: string | undefined;
</script>

<a href={url} target="_blank" rel="noreferrer" class="group w-full rounded-xl border border-gray-700 bg-gray-900/40 p-5 flex flex-col gap-2 hover:bg-gray-900 transition-colors duration-300">
  
  <div class="flex justify-between items-start w-full">
    <p class="font-bold text-lg text-gray-100 pr-4">{name}</p>
  </div>

  <div class="flex items-center gap-3">
    <p class="text-gray-400 text-sm font-mono">{date}</p>
    
    {#if role}
      <span class="px-2 py-0.5 rounded text-xs font-medium bg-blue-500/10 text-blue-400 border border-blue-500/20 whitespace-nowrap">
        {role}
      </span>
    {/if}
  </div>

</a>