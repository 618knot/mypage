<script lang="ts">
	import '../app.css';
	let { children } = $props();

	import Footer from '$lib/components/Footer.svelte';
	import { page } from '$app/stores';
</script>

<meta property="og:image" content="{$page.url.origin}/og-image.jpg" />

<div class="flex flex-col h-lvh">
	{@render children()}
	<Footer />
</div>
