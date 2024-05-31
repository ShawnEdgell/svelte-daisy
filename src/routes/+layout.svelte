<script>
	import '../app.css';
	import Navigation from '$lib/components/Navigation.svelte';
</script>

<div class="flex flex-col min-h-screen">
	<Navigation />
	<div class="flex-grow">
		<slot />
	</div>
</div>
