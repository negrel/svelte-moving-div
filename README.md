![package size](https://img.shields.io/github/size/nergel3/svelte-moving-div/src/index.svelte)
![npm version](https://img.shields.io/npm/v/svelte-moving-div?color=green)
# Svelte-moving-div

> A moving component for svelte js

### REPL Example

Check the basic [REPL example](https://svelte.dev/repl/73274fbd734d4164ab7fd281b84f5644?version=3.17.2).

![gif example](https://raw.githubusercontent.com/Nergel3/svelte-moving-div/master/resources/example.gif)

### Installation

```
npm install svelte-moving-div
```

### Getting started

```svelte
<script>
	// Example of svelte-moving-div component.
	// After 'npm install svelte-moving-div' you can use it :
	import MovingDiv from 'svelte-moving-div';
</script>

<MovingDiv>
	<h1>Hello World !</h1>
</MovingDiv>

<style>
	/* Bigger margin */
	:global(.moving-div) {
		padding: 2rem 5rem
	}
	
	/* Custom transition speed */
	:global(.moving-div > .inner-div) {
		transition: transform .25s!important
	}
</style>
```

### :stars: Show Your Support
Please give a :star: if this project helped you!

#### :scroll: License
MIT © Alexandre Negrel

