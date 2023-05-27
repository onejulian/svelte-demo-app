<script lang="ts">
	let count: number = 1;

	// the `$:` means 're-run whenever these values change'
	let doubled: number;
	let quadrupled: number;

	$: {
		doubled = count * 2;
		quadrupled = doubled * 2;
	}

	function handleClick(): void {
		count += 1;
	}
</script>

<button on:click={handleClick} class="nice-button">
	Count: {count}
</button>

<div class="m-5">
	<p>{count} * 2 = {doubled}</p>
	<p>{doubled} * 2 = {quadrupled}</p>
</div>

<style lang="postcss">
	.nice-button {
		@apply bg-blue-500 text-white font-bold py-2 px-4 rounded m-5;
	}
</style>
