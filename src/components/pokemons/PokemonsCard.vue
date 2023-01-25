<script>
import axios from "axios";
import pokemon from "./Pokemon.vue";
export default {
  name: "PokemonCards",
  components: { pokemon },
  data() {
    return {
      pokemons: [],
    };
  },
  created() {
    axios
      .get(
        "https://41tyokboji.execute-api.eu-central-1.amazonaws.com/dev/api/v1/pokemons?per=1100&page=1"
      )
      .then((res) => {
        this.pokemons = res.data.docs;
      });
  },
};
</script>

<template>
  <div class="row mx-0 p-2">
    <pokemon
      v-for="pokemon in this.pokemons"
      :key="pokemon._id"
      :name="pokemon.name"
      :image="pokemon.imageUrl"
      :number="pokemon.number"
      :type1="pokemon.type1"
      :type2="pokemon.type2"
    />
  </div>
</template>

<style scoped lang="scss">
div {
  justify-content: center;
}
</style>
