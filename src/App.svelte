<script>
	import {writable} from "svelte/store";
	import FunctionPropButton from "./FunctionPropButton.svelte";
	
	const count = writable(0);

	const increment = () => count.update(count => count + 1);
</script>

<style>
	h1 {
		color: purple;
	}
</style>

<h1>Hello {$count}!</h1>
<FunctionPropButton {increment} />

