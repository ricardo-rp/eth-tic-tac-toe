<script lang="ts" context="module">
	export type CellValue = '' | 'x' | 'o';
</script>

<script lang="ts">
	export let value: CellValue;
</script>

<div class="cell">{value}</div>

<style>
	.cell {
		display: flex;

		place-items: center;
		place-content: center;

		padding: 1em;
		border-radius: 10px;
		width: clamp(30px, 10vw, 70px);
		height: clamp(30px, 10vw, 70px);

		background: rgba(0, 0, 0, 0.1);

		transition: all 0.2s;
	}

	.cell:hover {
		background: rgba(0, 0, 0, 0.2);
	}
</style>
