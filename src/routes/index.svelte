<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Board from '$lib/components/board/Board.svelte';
	import { onMount } from 'svelte';
	import { defaultChainStore, web3 } from 'svelte-web3';

	// Connect to metamask
	onMount(() => defaultChainStore.setBrowserProvider());

	let balance;
	$: if ($web3) {
		balance = $web3.eth.getBalance('0x76fc18e74dd215467a5ed990ceb322c94df01de9');
	}
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
