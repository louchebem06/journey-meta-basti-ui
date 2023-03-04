<script lang="ts">
	import Logo from "$lib/Logo.svelte";
	import Menu from "$lib/Menu.svelte";
</script>

<header>
	<Logo />
	<Menu />
</header>

<style>
	header {
		--padding-border: 48px;
		width: calc(100vw - calc(var(--padding-border) * 2));
		position: fixed;
		top: 0;
		left: 0;
		padding: 24px var(--padding-border);
		background: rgba(255, 255, 255, 0.01);
		backdrop-filter: blur(26px);
		z-index: 100;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
</style>
