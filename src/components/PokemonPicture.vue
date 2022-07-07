<template>
  <div class="card-body">
    <div class="pokemon-container">
      <img :src="imgSrc" alt="Pokemon" class="hidden-pokemon" />
      <img v-if="showPokemon" :src="imgSrc" alt="Pokemon" class="fade-in" />
    </div>
    <h1 class="card-body-title">Who this is pokemon?</h1>
  </div>
</template>

<script>
export default {
  props: {
    pokemonId: {
      type: Number,
      required: true,
    },
    showPokemon: {
      type: Boolean,
      required: true,
      default: false,
    },
  },
  name: "PokemonPicture",
  computed: {
    imgSrc() {
      return `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/${this.pokemonId}.svg`;
    },
  },
};
</script>

<style scoped>
.card-body {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  border-bottom: 1px solid rgba(153, 153, 153, 0.383);
}

.card-body-title {
  margin-top: 2rem;
  text-transform: capitalize;
  font-size: 1.5rem;
}
.pokemon-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 200px;
  height: 200px;
  border: 5px solid white;
  border-radius: 50%;
  margin-top: calc(-100px - 5px);
  background-color: white;
}
.hidden-pokemon {
  filter: brightness(0);
  position: absolute;
}

img {
  width: 200px;
  height: 200px;
  user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -webkit-user-drag: none;
  -webkit-user-select: none;
}
</style>
