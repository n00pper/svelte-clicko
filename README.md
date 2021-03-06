# Svelte Clicko

Svelte `clickOutside` action, with support for multiple elements.

## Installation

```
npm i -D svelte-clicko
```

## Usage for a single element

```svelte
<script>
  import clickOutside from 'svelte-clicko';

  const onClickOutside = () => {
    // event handler
  }
</script>

<div use:clickOutside on:clickOutside={onClickOutside} />
```

## Usage for multiple elements

> `clickOutside` event will only fire if the click was outside every given element.

```svelte
<script>
  import clickOutside from 'svelte-clicko';

  let elementOne, elementTwo;

  const onClickOutside = () => {
    // event handler
  }
</script>

<div bind:this={elementOne}></div>
<div bind:this={elementTwo}></div>

<div
use:clickOutside={[elementOne, elementTwo]}
on:clickOutside={onClickOutside}>
</div>
```
