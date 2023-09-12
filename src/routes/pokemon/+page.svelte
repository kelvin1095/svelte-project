<script lang="ts">
  let types = [
    {
      id: 0,
      type: "",
    },
    {
      id: 1,
      type: "Normal",
    },
    {
      id: 2,
      type: "Fighting",
    },
    {
      id: 3,
      type: "Flying",
    },
    {
      id: 4,
      type: "Poison",
    },
    {
      id: 5,
      type: "Ground",
    },
    {
      id: 6,
      type: "Rock",
    },
    {
      id: 7,
      type: "Bug",
    },
    {
      id: 8,
      type: "Ghost",
    },
    {
      id: 9,
      type: "Steel",
    },
    {
      id: 10,
      type: "Fire",
    },
    {
      id: 11,
      type: "Water",
    },
    {
      id: 12,
      type: "Grass",
    },
    {
      id: 13,
      type: "Electric",
    },
    {
      id: 14,
      type: "Psychic",
    },
    {
      id: 15,
      type: "Ice",
    },
    {
      id: 16,
      type: "Dragon",
    },
    {
      id: 17,
      type: "Dark",
    },
    {
      id: 18,
      type: "Fairy",
    },
  ];

  let primaryType: string = "";
  let secondaryType: string = "";

  function printInputType() {
    console.log(primaryType, secondaryType);
  }

  let pokemonName: string = "";

  function printPokemonName() {
    console.log(pokemonName);
  }
</script>

<svelte:head>
  <title>Pokemon</title>
</svelte:head>

<main>
  <h1>My Pokemon Page!</h1>
  <div id="pokemonSelector">
    <h2>Select Pokemon Type</h2>

    <form id="selectType" on:submit={printInputType}>
      <label for="type-select-primary">Type 1:</label>
      <select name="Type" id="type-select-primary" bind:value={primaryType}>
        {#each types as type (type.id)}
          <option value={type.type}>
            {type.type}
          </option>
        {/each}
      </select>

      <label for="type-select-secondary">Type 2:</label>
      <select name="Type" id="type-select-secondary" bind:value={secondaryType}>
        {#each types as type (type.id)}
          <option value={type.type}>
            {type.type}
          </option>
        {/each}
      </select>

      <button type="submit">Submit</button>
    </form>
  </div>
</main>

<style lang="sass">

</style>
