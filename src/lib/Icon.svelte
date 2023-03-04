<script lang="ts">
	export let src: string;
	export let text: string;
</script>

<div class="icon">
	<!-- svelte-ignore a11y-img-redundant-alt -->
	<img {src} alt="icon picture" />
	<p>{text}</p>
</div>

<style>
	.icon {
		display: flex;
		flex-direction: column;
		max-width: 155px;
		gap: 18px;
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
