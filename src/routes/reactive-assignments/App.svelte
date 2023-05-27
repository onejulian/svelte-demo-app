<script lang="ts">
	let count = 0;

	function handleClick() {
		count += 1;
	}
</script>

<button on:click={handleClick} class="nice-button">
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>


<style lang="postcss">
	
	.nice-button {
		@apply bg-blue-500 text-white font-bold py-2 px-4 rounded m-5;
	}

</style>