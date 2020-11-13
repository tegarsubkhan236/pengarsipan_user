<script>
	import { Router, Link, Route } from "svelte-routing";
	import MainCollection from "./routes/MainCollection.svelte";
	import Landing from "./routes/Landing.svelte";
	import Detail from "./routes/Detail.svelte";

	export let url = "";
	// export let name;
</script>

<Router {url}>
	<Route path="/" component={Landing} />
	<Route path="main-collection" component={MainCollection} />
	<Route path="detail" component={Detail} />
</Router>
