<script>
	export let priorities = ['somehting','else'];
  let info =""
  function validate() {
    if (info != '') {
      console.log(info)
      priorities = [...priorities, info];
      info=""
    }
    
	}
</script>

{#each priorities as priority}
  <p>{priority}</p>
{/each}


<form on:submit|preventDefault={validate} >
	<input bind:value={info} type="text">
	<button type="submit">
		Add
	</button>
</form>
