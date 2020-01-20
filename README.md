![package size](https://img.shields.io/github/size/nergel3/svelte-moving-div/src/index.svelte)
![npm version](https://img.shields.io/npm/v/svelte-moving-div?color=green)
# Svelte-moving-div

> A moving component for svelte js

![gif example](https://github.com/Nergel3/svelte-moving-div/blob/master/resources/example.gif)

### Live demo

> Coming soon !

### Installation

```
npm install svelte-moving-div
```

### Getting started

```svelte
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
```

### :stars: Show Your Support
Please give a :star: if this project helped you!

#### :scroll: License
MIT © Alexandre Negrel

