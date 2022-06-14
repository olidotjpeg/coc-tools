<script lang="ts">
  import Input from './lib/Input.svelte';
  import DiceRoll from './lib/Diceroll.svelte';
</script>

<main>
  <Input />
  <DiceRoll />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  main {
    display: flex;
    flex-direction: column;
    height: 100vh;
    box-sizing: border-box;
    padding: 8px;
    margin: 0 auto;
  }
</style>
