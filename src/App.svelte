<script>
	import {Router,Link,Route} from 'svelte-routing'
	import Home from './views/Home.svelte'
	import Dev from './views/Dev.svelte'
	import Goweb from './views/Goweb.svelte'
	export let url = "";
</script>

<Router url="{url}">
	<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
		<div class="container-fluid">
			<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
				<span class="navbar-toggler-icon"></span>
			</button>
			<div class="collapse navbar-collapse" id="navbarNavAltMarkup">
				<div class="navbar-nav">
					<Link class="nav-link text-success " to="/">Home</Link>
					<Link class="nav-link" to="ingresar">ingresar</Link>
					<Link class="nav-link" to="goweb">Goweb</Link>
				</div>
			</div>
		</div>
	</nav>
	<main>
		<Route path="/ingresar">
			<Dev />
		</Route>
		<Route path="/goweb">
			<Goweb/>
		</Route>

		<Route path="/">
			<Home/>
		</Route>
	</main>
</Router>

<style>
</style>
