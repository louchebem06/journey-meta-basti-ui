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
	}

	.decoration {
		position: relative;
	}

	.row {
		position: absolute;
		left: 50%;
		top: 92%;
		transform: translateX(-9%);
	}

</style>
