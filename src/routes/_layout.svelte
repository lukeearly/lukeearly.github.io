<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	main {
		flex: 1 1 auto;
		position: relative;
		width: 750px;
		background-color: #f8f8f8;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
		height: 100%;
		border-left: 1px solid rgba(51, 51, 51, 0.2);
		border-right: 1px solid rgba(51, 51, 51, 0.2);
	}
	@media (max-width: 1000px) {
		main {
			width: 100%
		}
	}
	@media (min-width: 1500px) {
		main {
			width: 50%
		}
	}
</style>

<Nav {segment}/>

<main>
	<slot></slot>
</main>