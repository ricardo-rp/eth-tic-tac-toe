<script lang="ts">
	import Cell, { CellValue } from './cell/Cell.svelte';

	type Row = [CellValue, CellValue, CellValue];
	type GameBoard = [Row, Row, Row];

	const board: GameBoard = [
		['x', 'x', 'x'],
		['x', 'x', 'x'],
		['x', 'x', 'x']
	];
</script>

<div class="board">
	{#each board as row}
		{#each row as cell}
			<Cell value={cell} />
		{/each}
	{/each}
</div>

<style>
	.board {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		grid-template-rows: repeat(3, 1fr);
		gap: clamp(5px, 2vw, 20px);

		transition: all 0.2s;
	}
</style>
