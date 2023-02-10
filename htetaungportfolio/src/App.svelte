<svelte:head>
	<title>{name}</title>
</svelte:head>

<script>
	import Header from "./Components/Header/custom_header.svelte";
	import CustomFooter from "./Components/Footer/custom_footer.svelte";
	import ContentDisplayer from "./Components/Body/content_displayer.svelte";

	import VisitorCount from "./Components/visitor_count.svelte";

	export let name;
</script>

<main>
	<Header name={name}/>
	<ContentDisplayer name={name}/>
	<CustomFooter name={name}/>
</main>

<style>
	:global(body, html){
		margin: 0;
		padding: 0;
	}

	main {
		padding-top: 10vh;
		padding-bottom: 10vh;
		font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
		text-align: center;
		margin: 0;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	main :global(.FooterClass){
		font-family:'Courier New', Courier, monospace;
		position: fixed;
		bottom: 0;
		width: 100vw;
		height: 5vh;

		max-height: 10%;

		background-color: rgb(20, 0, 22);
		color:white;
		padding: 0;
	}

	main :global(.HeaderClass){

		width: 100vw;
		font-family:'Courier New', Courier, monospace;
		position:fixed;
		
		background-color: rgb(23, 0, 26);
		color: white;

		max-height: 10%;
		height: 10%;

		top: 0;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>