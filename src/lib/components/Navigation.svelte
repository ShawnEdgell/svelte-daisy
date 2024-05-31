<script lang="ts">
	import Login from './Login.svelte';
	let showModal = false;

	const routes = [
		{ name: 'Home', path: '/' },
		{ name: 'About', path: '/about' },
		{ name: 'Contact', path: '/contact' }
	];

	const toggleModal = () => {
		showModal = !showModal;
	};
</script>

<nav class="bg-gray-800 p-4 flex justify-between items-center">
	<ul class="flex space-x-4">
		{#each routes as { name, path }}
			<li>
				<a href={path} class="text-white hover:text-gray-400">{name}</a>
			</li>
		{/each}
	</ul>
	<button class="text-white bg-blue-500 hover:bg-blue-700 px-4 py-2 rounded" on:click={toggleModal}>
		Login
	</button>
	{#if showModal}
		<Login {toggleModal} />
	{/if}
</nav>
