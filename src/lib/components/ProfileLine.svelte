<script lang="ts">
  export let icon: string;
  export let alt: string;
</script>

<div class="flex gap-1.5">
  <img src={icon} alt={alt} />
  <p class="text-base font-medium"><slot /></p>
</div>
