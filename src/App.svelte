<script>
	import NavBar from "./Components/Navbar.svelte";
	import Tabs from "./Components/Tabs.svelte";
	let tabItems=['Morning','Afternoon','Night'];
	let activeItem='Morning';
	const tabChange=(e)=>
	{
     activeItem=e.detail;
	}
</script>

<main>
	<NavBar/>
	<Tabs {tabItems} {activeItem} on:tabChange={tabChange} />
</main>

<style>
	main {
		text-align: center;
		width:100%;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>