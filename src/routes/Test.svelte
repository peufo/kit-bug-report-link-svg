<script>
  import Svg from './Svg.svelte'

  export let title = ''
</script>

<h3>{title}</h3>

<svg
  viewBox="0 0 100 100"
  xmlns="http://www.w3.org/2000/svg"
  xmlns:xlink="http://www.w3.org/1999/xlink"
>
  <text x="50" y="15" text-anchor="middle">Native</text>
  <a href="/42">
    <circle cx="50" cy="50" r="20" />
  </a>
  <a href="/42">
    <text x="50" y="90" text-anchor="middle"> test link </text>
  </a>
</svg>

<Svg>
  <text x="50" y="15" text-anchor="middle">Component</text>
  <a href="/42">
    <circle cx="50" cy="50" r="20" />
  </a>
  <a href="/42">
    <text x="50" y="90" text-anchor="middle"> test link </text>
  </a>
</Svg>

<style>
  :global(svg) {
    border: solid gray 1px;
    border-radius: 4px;
    width: 200px;
  }
  :global(svg a) {
    fill: blue;
  }
</style>
