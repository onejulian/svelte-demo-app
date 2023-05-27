<script lang="ts">
	let count: number = 0;
	let maxCount: number = 5;

	$: {
		if (count > maxCount) {
			alert(`la cuenta ha llegado a su límite`);
			count = maxCount;
		}
	}

	function handleClick(): void {
		count += 1;
	}
</script>

<button on:click={handleClick} class="nice-button">
	Count: {count}
</button>

<div class="m-5">
	<p>Define límite</p>
	<input type="number" bind:value={maxCount} />
</div>

<style lang="postcss">
	.nice-button {
		@apply bg-blue-500 text-white font-bold py-2 px-4 rounded m-5;
	}
</style>
