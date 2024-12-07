<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import Footer from '$lib/components/Footer.svelte';
	import { page } from '$app/stores';
	import { base } from '$app/paths';
</script>

<meta property="og:image" content="{$page.url.origin}{base}/og-image.png" />

<div class="flex flex-col h-lvh">
	{@render children()}
	<Footer />
</div>
