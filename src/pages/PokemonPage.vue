<template>
  <article class="card">
    <img src="../assets/bg-pattern-card.svg" alt="" class="card-header" />

    <!-- TODO: img and question -->
    <PokemonPicture :pokemonId="150" :showPokemon="true" />

    <!-- TODO: Options-->
    <PokemonOptions />
  </article>
</template>

<script>
import PokemonOptions from "@/components/PokemonOptions.vue";
import PokemonPicture from "@/components/PokemonPicture.vue";

export default {
  name: "PokemonPage",
  components: {
    PokemonOptions,
    PokemonPicture,
  },
};
</script>

<style>
.card {
  background-color: white;
  width: 326px;
  border-radius: 16px;
  overflow: hidden;
  -webkit-box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
}
.card-header {
  width: 100%;
  display: block;
}
</style>
