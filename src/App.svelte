<script lang="ts">
	import Header from "./Header.svelte";
	import Navigation from "./Navigation.svelte";
	import Main from "./Main.svelte";
	import Footer from "./Footer.svelte";
</script>

<style>
	#app {
		display: grid;
		grid-template:
			"header header header" 5rem
			"nav nav nav" 5rem
			"main main main" minmax(calc(100vh - 12.5rem), auto)
			"footer footer footer" 2.5rem /
			25rem;
	}

	:global(#app > header) {
		grid-area: header;
	}

	:global(#app > nav) {
		grid-area: nav;
	}

	:global(#app > main) {
		grid-area: main;
	}

	:global(#app > footer) {
		grid-area: footer;
	}
</style>

<div id="app">
	<Header />
	<Navigation />
	<Main />
	<Footer />
</div>
