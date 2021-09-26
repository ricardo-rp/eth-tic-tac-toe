<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Board from '$lib/components/board/Board.svelte';
</script>

<svelte:head>
	<title>Catchy name</title>
</svelte:head>

<section>
	<h1>Catchy name</h1>

	<Board />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}
</style>
