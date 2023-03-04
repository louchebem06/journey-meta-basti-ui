<script>
	import LineUnion from "$lib/LineUnion.svelte";
</script>

<div class="hero">
	<img draggable="false" src="/img/background1.png" alt="background img" />
	<img draggable="false" src="/img/girlVR.png" alt="girl vr" />
	<LineUnion />
</div>

<style>
	.hero {
		width: 100vw;
		position: relative;
	}

	.hero img:nth-child(1) {
		width: 100%;
	}

	.hero img:nth-child(2) {
		position: absolute;
		left: 50%;
		bottom: 12.3%;
		transform: translateX(-54%);
		height: 40%;
		z-index: 2;
	}
</style>
