<script>
  import RowUnion from "./RowUnion.svelte";
</script>

<div class="presentation">
	<div class="content">
		<div class="text">
			<h1>.une simple phrase et vous décollez</h1>
			<p>
				Demandez à notre intelligence artificielle où vous souhaitez voyager et nous
				nous chargerons de vous guider vers la destination qui vous convient. Grâce
				à sa commande vocale, il est facile de s'adapter à votre style de vie et de
				répondre à vos envies du moment. N'attendez plus et dites-lui où vous
				souhaitez aller !
			</p>
		</div>
		<div class="chat">
			<div class="left">
				<p>Bonjour</p>
			</div>
			<div class="right">
				<p>Bonjour Clara</p>
			</div>
			<div class="left">
				<p>Où voulez-vous aller aujourd'hui ?</p>
			</div>
			<div class="right">
				<p>Je ne sais pas, qu'est-ce que vous suggérez ?</p>
			</div>
			<div class="left">
				<p class="left">Nous pourrions aller à la plage ?</p>
			</div>
			<div class="right">
				<p>D'accord, allons-y !</p>
			</div>
		</div>
	</div>
	<!-- svelte-ignore a11y-img-redundant-alt -->
	<img draggable="false" src="/img/vr-headset.png" alt="vr picture decoration" />
	<div class="row">
		<RowUnion />
	</div>
</div>

<style>
	.presentation {
		min-height: 100vh;
		font-style: normal;
		color: #FFFFFF;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 34px;
		position: relative;
		margin-left: calc(58px * 2);
	}
	.presentation h1 {
		font-weight: 500;
		font-size: 32px;
		line-height: 39px;
		max-width: 313px;
	}

	.presentation p {
		font-family: 'Epilogue';
		font-weight: 300;
		font-size: 14px;
		line-height: 21px;
		max-width: 372px;
	}

	.text {
		display: flex;
		gap: 16px;
		flex-direction: column;
	}

	.presentation img {
		max-width: 482px;
		max-height: 482px;
		border-radius: 8px;
	}

	.content {
		z-index: 1;
		margin-right: -58px;
		position: relative;
	}

	.chat {
		position: absolute;
		display: flex;
		gap: 8px;
		flex-direction: column;
		top: calc(100% + 43px);
		width: 400px;
	}

	.left p, .right p {
		font-family: 'ClashDisplay-Variable';
		font-style: normal;
		font-weight: 400;
		font-size: 14px;
		line-height: 17px;
		color: #FFFFFF;
		padding: 8px 16px;
		display: inline-block;
		border: 1px solid #FFFFFF;
		border-radius: 48px;
	}

	.right p {
		background: #FFFFFF;
		color: black!important;
		float: right;
	}

	.row {
		position: absolute;
		top: 3%;
		left: 50%;
		transform: translateX(-33%);
	}

	@media screen and (max-width: 768px) {
		.presentation {
			justify-content: space-between;
			margin-left: 0;
			padding-left: 5%;
		}
		.presentation img {
			width: 50vw;
		}

		.presentation .content {
			margin-right: 0;
		}

		.chat {
			max-width: 400px;
			width: 100vw;
		}

		.row {
			transform: translateX(-5%);
		}
	}

	@media screen and (max-width: 425px) {
		.presentation {
			flex-direction: column-reverse;
			justify-content: center;
		}

		.chat {
			position: relative;
			width: 90vw;
		}
	}
</style>
