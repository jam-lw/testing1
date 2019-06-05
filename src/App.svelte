<script>
	import {writable} from "svelte/store";
	import IncrementButton from "./IncrementButton.svelte";
	import ResetButton from "./ResetButton.svelte";
	
	const count = writable(0);

	const increment = () => count.update(count => count + 1);
	const reset = () => count.set(0);
</script>

<style>
	h1 {
		color: crimson;
	}
</style>

<h1>Hello {$count}!</h1>
<IncrementButton {increment} />
<ResetButton {reset} />
