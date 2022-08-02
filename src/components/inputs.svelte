<script>
	export let priorities = [];
  let info =""
  function validate() {
    if (info != '') {
      console.log(info)
      priorities = [...priorities, info];
      info=""
    }
	}
  function remove(item) {
    alert(item)
  priorities = priorities.filter((value) => value.id !== item.id);
  };
</script>

{#each priorities as priority}
<div let:dataItem let:item>
  <span>{priority}</span><div class="spacing"></div><span on:click={() => remove(priority)}>X</span>
</div>

{/each}


<form on:submit|preventDefault={validate} >
	<input bind:value={info} type="text">
	<button type="submit">
		Add
	</button>
</form>
