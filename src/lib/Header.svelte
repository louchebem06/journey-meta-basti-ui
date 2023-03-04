<script lang="ts">
	import Logo from "$lib/Logo.svelte";
</script>

<header>
	<Logo />
</header>

<style>
	header {
		width: 100vw;
		position: fixed;
		top: 0;
		left: 0;
		padding: 24px 48px;
		background: rgba(255, 255, 255, 0.01);
		backdrop-filter: blur(26px);
		z-index: 100;
	}
</style>
