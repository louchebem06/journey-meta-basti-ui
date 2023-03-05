<script>
	import LineUnion from "$lib/LineUnion.svelte";
	import Button from "$lib/Button.svelte";
</script>

<div class="hero">
	<img draggable="false" src="/img/background1.png" alt="background img" />
	<img draggable="false" src="/img/girlVR.png" alt="girl vr" />
	<LineUnion />
	<div class="button">
		<Button border>s’évader</Button>
	</div>
</div>

<style>
	.hero {
		width: 100vw;
		position: relative;
		overflow: hidden;
	}

	.hero img {
		-webkit-mask-image: linear-gradient(180deg, #000000 74%, rgba(0, 0, 0, 0) 100%);
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

	.button {
		position: absolute;
		bottom: 10px;
		left: 50%;
		transform: translateX(-50%);
	}
</style>
