<script>
  export let name;
	let count = 0

  function increaseCount() {
		count += 1;
	}
</script>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>

<main>
  <h1>{name}</h1>
  
	<button on:click={increaseCount}>
		{#if count === 0 }
		<span>Click here</span>
		{:else}
		<span>Clicked {count} {count === 1 ? 'time' : 'times'}</span>
		{/if}
	</button>
</main>
