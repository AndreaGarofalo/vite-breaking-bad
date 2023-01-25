<script>
import PokemonsCards from "./pokemons/PokemonsCard.vue";
export default {
  name: "AppMain",
  components: { PokemonsCards },
};
</script>

<template>
  <div class="container">
    <div class="pokemons">
      <div class="pokemon-list">
        <PokemonsCards />
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
.pokemons {
  height: 78vh;
  background-color: white;
  border-radius: 25px;
  margin-top: 10rem;

  .pokemon-list {
    height: 100%;
    width: 100%;
    background-color: darkgray;
    overflow-x: auto;
  }
}
</style>
