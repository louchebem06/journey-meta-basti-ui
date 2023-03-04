<div class="row">
	{#each [0,1,2,3,4,5,6,7,8,9,10,11,12,13] as i}
		<img src="/img/union.png" alt="union logo" />
	{/each}
</div>

<style>
	.row {
		display: flex;
		flex-direction: column;
		height: 43vh;
	}

	.row img {
		width: 10.1%;
		opacity: 0.1;
		transform: rotate(90deg);
	}
</style>
