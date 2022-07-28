<script>
	import Inputs from "../src/components/inputs.svelte"

	let inputs = []
</script>

<h1>Make time</h1>
<p>This are the inputs {inputs[0]}</p>
<Inputs bind:priorities={inputs}/>

<style>
	
</style>