<script>
	import Inputs from "../src/components/inputs.svelte"

	let inputs = []
</script>

<h1>Make time</h1>
<p>These are the inputs</p>
<Inputs bind:priorities={inputs}/>

<style>
	
</style>