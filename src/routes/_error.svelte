<script>
	export let status;
	export let error;

	const dev = process.env.NODE_ENV === 'development';
</script>

<svelte:head>
	<title>{status}</title>
</svelte:head>

<div class="showcase">
	<span>
		<h1>{status}</h1>
		<h3 style="color: white;">{error.message}</h3>
		{#if dev && error.stack}
			<pre style="color: white; margin-top: 48px;">{error.stack}</pre>
		{/if}
	</span>
</div>
