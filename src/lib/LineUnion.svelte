<div class="line">
	{#each [0,1,2,3,4,5,6] as i}
		<img src="/img/union.png" alt="union logo" />
	{/each}
</div>

<style>
	.line {
		position: absolute;
		left: 0;
		bottom: 25%;
		z-index: 1;
		display: flex;
		width: 100%;
		justify-content: center;
	}

	.line img {
		width: 12%;
		opacity: 0.25;
	}
</style>
