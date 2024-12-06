<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import Footer from '$lib/components/Footer.svelte';
</script>

<div class="flex flex-col h-lvh">
	{@render children()}
	<Footer />
</div>
