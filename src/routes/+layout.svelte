<script>
	import '$lib/app.css';
	import faviconUrl from '$lib/favicon.svg?url';

	const { children } = $props();
</script>

<svelte:head>
    <link rel="icon" href={faviconUrl} sizes="any" type="image/svg+xml">
</svelte:head>

{@render children()}
