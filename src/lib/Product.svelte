<script lang="ts">
  import Button from "./Button.svelte";

	export let price: number;
	export let name: string;
	export let src: string;
	export let href: string = "#";
	export let elements: string[];
</script>

<div class="product">
	<!-- svelte-ignore a11y-img-redundant-alt -->
	<img {src} alt="picture product" />
	<div class="content">
		<h3>{name}</h3>
		<ul>
			{#each elements as element}
				<li>{element}</li>
			{/each}
		</ul>
		<p>{price}€/mois</p>
		<div class="button">
			<Button {href} border>c'est parti</Button>
		</div>
	</div>
</div>

<style>
	.product {
		width: 242px;
		height: 471px;
		overflow: hidden;
		border-radius: 8px;
		background-color: transparent;
		transition: 0.5s background-color;
	}

	.product h3 {
		font-style: normal;
		font-weight: 500;
		font-size: 24px;
		line-height: 30px;
		color: #FFFFFF;
	}

	.product ul li {
		font-family: 'Epilogue';
		font-style: normal;
		font-weight: 300;
		font-size: 14px;
		line-height: 21px;
		color: #FFFFFF;
	}

	.product p {
		font-style: normal;
		font-weight: 500;
		font-size: 15px;
		line-height: 18px;
		color: #FFFFFF;
	}

	.product ul {
		margin-left: 20px;
	}

	.content {
		display: flex;
		flex-direction: column;
		gap: 16px;
		width: 226px;
		height: 224px;
	}

	.content {
		margin-left: 20px;
	}

	.product img {
		width: 100%;
		height: 90%;
		border-radius: 8px;
		object-fit: cover;
		transition: 0.5s height;
	}

	.product:hover img {
		height: 57%;
		transition: 0.5s height;
	}

	.product:hover {
		background-color: rgba(0, 0, 0, 0.05);
		transition: 0.5s background-color;
	}
</style>
