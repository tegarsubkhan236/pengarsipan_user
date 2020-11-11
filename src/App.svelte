<script>
	import { Router, Link, Route } from "svelte-routing";
	import Landing from "./routes/Landing.svelte";

	export let url = "";
	// export let name;
</script>

<Router {url}>
	<nav>
		<Link to="/">Landing</Link>
	</nav>
	<div>
		<Route path="/" component={Landing} />
	</div>
</Router>
