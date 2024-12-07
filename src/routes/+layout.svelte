<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import Footer from '$lib/components/Footer.svelte';
	import { page } from '$app/stores';
	import { base } from '$app/paths';
</script>

<svelte:head>
	<meta property="og:title" content="618knot" />
	<meta property="og:description" content="About 618knot." />
	<meta property="og:image:type" content="image/png">
	<meta property="og:image:width" content="1200">
	<meta property="og:image:height" content="630">
	<meta property="og:image" content="{$page.url.origin}{base}/og-image.png" />
</svelte:head>

<div class="flex flex-col h-lvh">
	{@render children()}
	<Footer />
</div>
