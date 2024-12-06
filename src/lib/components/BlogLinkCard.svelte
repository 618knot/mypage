<script lang="ts">
  import externalLink from "$lib/assets/icon/externallink.svg";

  export let blogName: string;
  export let account: string;
  export let url: string;
</script>

<a href={url} target="_blank" rel="noreferrer" class="w-full rounded-md border border-gray-200 p-5 text-base flex gap-7 justify-center hover:bg-gray-800 transition-colors duration-300">
  <p>{blogName}</p>
  <p>{account}</p>
  <img src={externalLink} alt="">
</a>
