<script lang="ts">
	import Button from "./Button.svelte";

	let scrolling: any;
	function scroll(e: any) {
		const firstChild = e.srcElement.children[0];
		if (firstChild.width <= e.srcElement.scrollLeft) {
			e.srcElement.appendChild(firstChild);
			e.srcElement.style.scrollBehavior = "initial";
			e.srcElement.scroll(0, 0);
			e.srcElement.style.scrollBehavior = "smooth";
		}
	}
</script>

<div class="carouselle">
	<div class="content">
		<h3>.choisissez votre destination</h3>
		<p>
			Choisissez votre destination et laissez-vous inspirer.
			Paris, la ville de l’amour, n’est-ce pas un pays parfait
			pour votre lune de miel ?<br/>
			Rien n’est plus romantique que de flâner dans les rues de la ville
			lumière, déguster une crêpe au chocolat et profiter de la vue
			magnifique depuis la tour Eiffel.
		</p>
		<span>
			<Button border>découvrir les destinations</Button>
		</span>
	</div>
	<div bind:this={scrolling} on:scroll={scroll} class="scrolling">
		<img src="/img/scrolling/variant1.png" alt="" />
		<img src="/img/scrolling/variant2.png" alt="" />
		<img src="/img/scrolling/variant3.png" alt="" />
		<img src="/img/scrolling/variant4.png" alt="" />
	</div>
</div>

<style>
	.carouselle {
		margin-top: 200px;
		padding: 120px 0;
		position: relative;
	}

	.content {
		position: absolute;
		bottom: 340px;
		left: 50%;
		max-width: 379px;
		transform: translateX(-150%);
		display: flex;
		flex-direction: column;
		gap: 16px;
		font-style: normal;
		color: #FFFFFF;
		z-index: 1;
	}

	.content h3 {
		font-weight: 500;
		font-size: 32px;
		line-height: 39px;
	}

	.content p {
		font-family: 'Epilogue';
		font-weight: 300;
		font-size: 14px;
		line-height: 21px;
		margin-bottom: 10px;
	}

	.scrolling {
		-webkit-mask-image: linear-gradient(90deg, rgba(0, 0, 0, 0) 0%, #000000 50%);
		display: flex;
		overflow-x: scroll;
		scroll-behavior: smooth;
		margin-left: 18%;
	}

	.scrolling img {
		-webkit-mask-image: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 48.78%, rgba(0, 0, 0, 0) 100%);
		object-fit: cover;
		height: 409px;
	}
</style>
