<main>
	<MovingDiv>
		<h1>
			Hello World !
		</h1>
	</MovingDiv>
</main>

<script>
import MovingDiv from 'svelte-moving-div';
</script>

<style>
/* Extending the the moving div */
:global(.moving-div) {
  padding: 2rem;
}


/* Adding transition to slow down */
:global(.moving-div) > :global(.inner-div) {
  transition: transform .4s cubic-bezier(.04, .48, .98, .8)
}
</style>