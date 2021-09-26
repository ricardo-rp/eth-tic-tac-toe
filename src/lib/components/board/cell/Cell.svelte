<script lang="ts" context="module">
	export type CellValue = '' | 'x' | 'o';
</script>

<script lang="ts">
	export let value: CellValue;

	const className = `cell ${!value && 'empty'}`;
</script>

<div class={className}>{value}</div>

<style>
	.cell {
		display: flex;

		place-items: center;
		place-content: center;

		padding: 1em;
		border-radius: 10px;
		width: clamp(30px, 10vw, 70px);
		height: clamp(30px, 10vw, 70px);

		background: rgba(0, 0, 0, 0.2);
		border: solid 2px rgba(0, 0, 0, 0);

		transition: all 0.2s;
	}

	.empty {
		background: rgba(0, 0, 0, 0.1);
	}
	
	.empty:hover {
		background: rgba(0, 0, 0, 0.2);
		border: solid 2px darkgray;
		cursor: pointer;
	}

	.empty:active {
		background: lightgray;
		border: solid 2px lightgray;
	}
</style>
