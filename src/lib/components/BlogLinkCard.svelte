<script lang="ts">
  export let blogName: string;
  export let account: string;
  export let url: string;
</script>

<a href={url} target="_blank" rel="noreferrer" class="w-full rounded-xl border border-gray-700 bg-gray-900/40  p-5 text-base flex gap-7 justify-center items-center hover:bg-gray-900 transition-colors duration-300">
  <p>{blogName}</p>
  <p class="text-gray-400">{account}</p>
</a>
