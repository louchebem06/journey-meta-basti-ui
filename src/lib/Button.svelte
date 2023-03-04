<script lang="ts">
	export let href: string = "#";
	export let border: boolean = false;
</script>

<a class:border={border} {href}>
	<slot></slot>
</a>

<style>
	a {
		text-decoration: none;
		color: #FFFFFF;
		border: 1px solid transparent;
		padding: 8px 16px;
		border-radius: 48px;
		font-style: normal;
		font-weight: 400;
		font-size: 14px;
		line-height: 17px;
		text-align: center;
	}

	.border {
		border: 1px solid #FFFFFF!important;
	}

	a:hover {
		background-color: #FFFFFF;
		color: black;
	}
</style>