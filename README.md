![](https://img.shields.io/github/size/nergel3/svelte-moving-div/src/index.svelte)
![](https://img.shields.io/npm/v/svelte-moving-div?color=green)
# Svelte-moving-div

> A moving component for svelte js

### Live demo

> Coming soon !

### Installation

```
npm install --save-dev svelte-mui
```

### Getting started

```svelte
<script>
import MovingDiv from 'svelte-moving-div';
</script>

<div id="my-application">
  <MovingDiv>
    <h1>
      Hello World!
    </h1>
  </MovingDiv>
</div>

<style>

// The mouse must hover the moving-div
:global(.moving-div) {
  padding: 2rem;
}

// Adding transition to slow down
:global(.moving-div) > :global(.inner-div) {
  transition: transform .4s cubic-bezier(.04, .48, .98, .8)
}
</style>
```

### :stars: Show Your Support
Please give a :star: if this project helped you!

#### :scroll: License
MIT © Alexandre Negrel

