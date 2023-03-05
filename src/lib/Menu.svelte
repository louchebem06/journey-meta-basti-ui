<script lang="ts">
	import Button from "$lib/Button.svelte";
	let active: boolean = false;
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div class="menu-mobile" class:active-mobile={active} on:click={() => {active = !active}}></div>

<div class="menu" class:active={active}>
	<Button>nos service</Button>
	<Button>nos destinations</Button>
	<Button>nos offres</Button>
	<Button border>votre espace</Button>
</div>

<style>
	.menu {
		display: flex;
		gap: 32px;
	}

	.menu-mobile {
		width: 20px;
		height: 2px;
		background-color: white;
		display: none;
		z-index: 10;
		position: relative;
		opacity: 1;
		transition: 0.2s top;
		transition: 0.2s transform;
	}

	.menu-mobile:after, .menu-mobile:before {
		width: 20px;
		height: 2px;
		background-color: white;
		display: none;
		position: absolute;
		left: 0;
		width: 100%;
		height: 100%;
		content: " ";
		transition: 0.2s top;
		transition: 0.2s transform;
	}

	.menu-mobile:after {
		top: 5px;
	}

	.menu-mobile:before {
		top: -5px;
	}

	.active-mobile {
		transform: rotate(45deg);
		transition: 0.2s transform;
	}

	.active-mobile::after {
		top: 0;
		transform: rotate(90deg);
		transition: 0.2s top;
		transition: 0.2s transform;
	}

	.active-mobile::before {
		top: 0;
		transition: 0.2s top;
	}

	@media screen and (max-width: 768px) {
		.menu-mobile, .menu-mobile:before, .menu-mobile:after {
			display: block;
		}

		.menu {
			position: fixed;
			left: -100%;
			top: 0;
			background: rgba(0, 0, 0, 0.9);
			flex-direction: column;
			width: 50%;
			padding: 5%;
			height: 100vh;
			align-items: center;
			justify-content: center;
			transition: 1s left;
			z-index: 0;
		}

		.active {
			left: 0;
			transition: 1s left;
		}
	}

	@media screen and (max-width: 425px) {
		.menu {
			width: 90%;
		}
	}
</style>
