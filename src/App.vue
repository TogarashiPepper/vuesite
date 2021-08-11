<script>
	export default {
		name: "app",
		data() {
			return {
				isDreamStan: Boolean(Math.floor(Math.random() * 5)),
			};
		},
		methods: {
			getIsDreamStan() {
				this.isDreamStan = Boolean(Math.floor(Math.random() * 5));
			}
		}
	}
</script>

<template>
	<div>
		<h1>you {{isDreamStan ? 'are' : 'aren\'t'}} a dream stan</h1>
		<button class="btn" v-on:click="getIsDreamStan">reroll</button>
	</div>
</template>

<style>
	html {
		background-color: #36393f;
		display: flex;
		align-items: center;
		justify-content: center;
		height: 100vh;
	}
	h1 {
		color: whitesmoke;
	}
	.btn {
		padding-left: 40px;
		padding-right: 40px;
		border-radius: 1px;
		font-size: 20px;
		order: 2;
		flex: 0 0 120px;
		border: 2px solid #00AA66;
	}
</style>
