<script lang="ts">
	export let src: string;
	export let text: string;
</script>

<div class="icon">
	<div class="img">
		<!-- svelte-ignore a11y-img-redundant-alt -->
		<img draggable="false" {src} alt="icon picture" />
	</div>
	<p>{text}</p>
</div>

<style>
	.icon {
		display: flex;
		flex-direction: column;
		width: 155px;
		gap: 18px;
	}

	.icon img {
		max-height: 100%;
	}

	.img {
		height: 112px;
		width: 100%;
		text-align: center;
	}

	.icon p {
		font-family: 'Epilogue';
		font-style: normal;
		font-weight: 500;
		font-size: 14px;
		line-height: 21px;
		text-align: center;
		color: #FFFFFF;
	}
</style>
