<template>
  <h1>Who is this pokemon?</h1>
  <!-- TODO: img -->
  <PokemonPicture />
  <!-- TODO: Options-->
  <PokemonOptions />
</template>

<script>
import PokemonOptions from '@/components/PokemonOptions.vue'
import PokemonPicture from '@/components/PokemonPicture.vue'

export default {
  name: 'PokemonPage',
  components: {
    PokemonOptions,
    PokemonPicture
  }
}
</script>

<style>

</style>