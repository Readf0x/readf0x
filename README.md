### Aspiring software engineer with *significant* web dev experience
Check out this [sweet animation](https://svelte.dev/repl/58015a8320bc440d8ba64fb58de7d742?version=4.2.11)

<details>
  <summary>Or render it yourself in svelte</summary>

```svelte
<script>
  var showcaseElems = Array.from({length: 9}, (_, i) => (i + 1) * 100)
  var sweet = [
    "s",
    "w",
    "e",
    "e",
    "t",
  ]
  var sweetI = Array.from({length: sweet.length}, (_, i) => i + 1)

  setInterval(() => {
    showcaseElems.push(900 - showcaseElems.shift())
    showcaseElems = showcaseElems
    sweetI.push(sweetI.length - sweetI.shift())
    sweetI = sweetI
  }, 100)
</script>

<svelte:head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Noto+Sans:ital,wdth,wght@0,62.5..100,100..900;1,62.5..100,100..900&display=swap" rel="stylesheet">
</svelte:head>

<h1>
  Look at this
  {#each sweet as l, i}
    <i style:font-variation-settings="'wdth' {((37.5 / 4) * (sweetI[i])) + 62.5}, 'wght' {((800 / 4) * (sweetI[i])) + 100}">{l[0]}</i>
  {/each}
  animation
</h1>

<div class="variable-showcase">
  {#each showcaseElems as i}
  <p class="variable-showcase-item" style:font-weight={i}>Animation</p>
  {/each}
</div>

<style>
  * {
    font-family: "Noto Sans";
    transition: 0.5s;
  }
  .variable-showcase {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100px;
  }
  .variable-showcase-item {
    margin: 0;
  }
</style>
```

</details>
