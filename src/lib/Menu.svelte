<script lang="ts">
  let marshmallows: any = [
      {
          name: "Fluffy", 
          priceCents: 299
      },
      {
          name: "Not as fluffy", 
          priceCents: 199
      }
  ]
  export let addCartItem;
</script>

{#each marshmallows as marshmallow}
    <button on:click={addCartItem(marshmallow)}>
        {marshmallow.name}<br>${marshmallow.priceCents / 100.0}
    </button>
{/each}

<style>
  button {
    font-family: inherit;
    font-size: inherit;
    padding: 1em 2em;
    color: #ff3e00;
    background-color: rgba(255, 62, 0, 0.1);
    border-radius: 2em;
    border: 2px solid rgba(255, 62, 0, 0);
    outline: none;
    width: 200px;
    font-variant-numeric: tabular-nums;
    cursor: pointer;
  }

  button:focus {
    border: 2px solid #ff3e00;
  }

  button:active {
    background-color: rgba(255, 62, 0, 0.2);
  }
</style>
