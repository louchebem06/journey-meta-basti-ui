<script lang="ts">
	import RowUnion from "./RowUnion.svelte";
</script>

<div class="decoration">
	<img src="/img/background2.png" alt="background decoration" />
	<div class="row">
		<RowUnion />
	</div>
</div>

<style>
	img {
		max-width: 100%;
		-webkit-mask-image: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 33.16%, #000000 57.64%, rgba(0, 0, 0, 0) 100%);
	}

	.decoration {
		position: relative;
	}

	.row {
		position: absolute;
		left: 50%;
		top: 85%;
		transform: translateX(-9%);
	}

</style>
