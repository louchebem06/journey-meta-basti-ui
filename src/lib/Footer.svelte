<script>
  	import Button from "./Button.svelte";
	import Logo from "./Logo.svelte";
 	import RowUnion from "./RowUnion.svelte";

</script>
<footer>
	<img src="/img/background3.png" alt="background 3" />
	<div class="row">
		<RowUnion />
	</div>
	<div class="footer">
		<Logo />
		<p>
			Design by <a href="https://www.youtube.com/@BastiUi">Basti UI</a>
			<br/>
			Implement by <a href="https://github.com/louchebem06">louchebem06</a>
		</p>
		<Button border>on rentre ?</Button>
	</div>
</footer>

<style>
	footer {
		margin-top: -20%;
		position: relative;
		-webkit-mask-image:  linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
		background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, #000000 100%);
	}

	img {
		width: 100%;
		mix-blend-mode: overlay;
	}

	.footer {
		--padding-border: 48px;
		width: calc(100vw - calc(var(--padding-border) * 2));
		padding: 24px var(--padding-border);
		z-index: 100;
		display: flex;
		align-items: center;
		justify-content: space-between;
		position: absolute;
		bottom: 0;
		left: 0;
		flex-wrap: wrap;
		gap: 100px;
	}

	footer p, footer p a {
		font-style: normal;
		font-weight: 400;
		font-size: 12px;
		line-height: 15px;
		color: #FFFFFF;
		text-align: center;
	}

	.footer p a {
		text-decoration: underline;
		font-weight: 500;
	}

	.row {
		position: absolute;
		bottom: 10%;
		left: 50%;
		transform: translateX(-3%);
	}

	@media screen and (max-width: 700px) {
		footer {
			margin-top: 0;
		}

		.footer {
			flex-direction: column;
			align-items: center;
			justify-content: center;
			gap: 20px;
		}
	}
</style>
