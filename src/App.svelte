<script>
	import NavBar from './components/NavBar.svelte'
	import Presentation from './pages/Presentation.svelte'
	import Projects from './pages/Projects.svelte'
</script>

<main>
	<NavBar/>
	<Presentation/>
	<Projects/>
</main>

<style>
	
	



	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>