<script>
	import { Router, Link, Route } from "svelte-routing";
	import Container from "./routes/Container.svelte";
	import Landing from "./routes/Landing.svelte";

	export let url = "";
	// export let name;
</script>

<Router {url}>
	<Route path="/" component={Landing} />
	<Route path="container" component={Container} />
	<Route path="test" component={Landing} />
</Router>
