<script lang="ts">
	import Icon from "$lib/Icon.svelte";
</script>

<div class="block">
	<h1>.une méthode de voyage respectueuse</h1>
	<p>
		Pour éviter les émissions de CO2, les vols sont à éviter. Mais pas les
		voyages ! Grâce à la réalité virtuelle, il est possible de découvrir
		des paysages de toute la planète sans bouger de chez soi. Il suffit de
		disposer d’un casque de réalité virtuelle et d’une manette de jeu. Une
		fois équipés de cet ensemble, l’utilisateur peut naviguer dans l’espace
		virtuel autour de lui comme s’il se trouvait en plein cœur de la jungle
		amazonienne, dans les ruelles de Rio de Janeiro ou sur les bords de la
		mer Morte.
	</p>
	<div class="icon">
		<Icon src="/img/icon/icon1.png" text={"Réduisez les\nemissions de CO2"} />
		<Icon src="/img/icon/icon2.png" text={"Plongez vous dans\nun monde immersif"} />
		<Icon src="/img/icon/icon3.png" text={"Voyagez sans bouger\nde chez vous"} />
	</div>
</div>

<style>
	.block {
		margin: 15vw auto 54px auto;
		max-width: 720px;
		font-style: normal;
		color: #FFFFFF;
		/* min-height: 100vh; */
	}

	.icon {
		display: flex;
		justify-content: space-around;
		margin: auto;
	}

	.block h1 {
		max-width: 355px;
		font-weight: 500;
		font-size: 32px;
		line-height: 39px;
		margin-bottom: 29px;
	}

	.block p {
		max-width: 516px;
		font-family: 'Epilogue';
		font-weight: 400;
		font-size: 14px;
		line-height: 21px;
		margin-bottom: 69px;
	}

	@media screen and (max-width: 768px) {
		.block {
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
			margin: 10% auto;
			width: 90vw;
			min-height: 0;
			gap: 30px;
		}

		.block p {
			margin-bottom: 0;
		}

		.block h1 {
			margin-bottom: 0;
		}

		.icon {
			flex-wrap: wrap;
		}
	}
</style>
