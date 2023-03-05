<script>
	import Product from "$lib/Product.svelte";
</script>


<div class="product">
	<h1>.nos offres</h1>
	<span>
		<Product
			src="/img/product/product1.png"
			name=".starter" price={4}
			elements={
				[
					"30 min de voyage",
					"1 profil",
					"publicité"
				]
			}
		/>
		<Product
			src="/img/product/product2.png"
			name=".traveler" price={9}
			elements={
				[
					"1h de voyage",
					"3 profils",
					"pas de publicité"
				]
			}
		/>
		<Product
			src="/img/product/product3.png"
			name=".explorer" price={19}
			elements={
				[
					"voyage et profil illimités",
					"pas de publicité",
					"casque prenium"
				]
			}
		/>
	</span>
</div>

<style>
	.product {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding-bottom: 168px;
		gap: 45px;
		background: radial-gradient(50% 50% at 50% 50%, rgba(0, 0, 0, 0.6) 0%, rgba(0, 0, 0, 0) 100%);
	}

	.product span {
		display: flex;
		gap: 8px;
		z-index: 10;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
	}

	.product h1 {
		margin-top: 84px;
		font-style: normal;
		font-weight: 500;
		font-size: 32px;
		line-height: 39px;
		color: #FFFFFF;
	}
</style>
