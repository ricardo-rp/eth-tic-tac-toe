<script lang="ts">
	type Cell = '' | 'x' | 'o';
	type Row = [Cell, Cell, Cell];
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
			<button class="cell">{cell}</button>
		{/each}
	{/each}
</div>

<style>
	.board {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		grid-template-rows: repeat(3, 1fr);
		gap: 1em;

		transition: all 0.2s;
	}

	.cell {
		padding: 1em;
		border-radius: 10px;
		width: clamp(30px, 10vw, 50px);
		height: clamp(30px, 10vw, 50px);

		background: rgba(0, 0, 0, 0.1);

		transition: all 0.2s;
	}
	.cell:hover {
		background: rgba(0, 0, 0, 0.2);
	}
</style>
