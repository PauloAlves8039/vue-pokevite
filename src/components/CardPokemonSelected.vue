<script setup>
const pokemon = defineProps(["name", "xp", "height", "img", "loading"]);

</script>

<template>
  <div class="card cardPokemonSelected" 
  :class="loading ? '' : 'animate__animated animate__flipInX'"
  >
    <img 
      :src="pokemon.img" 
      class="card-img-top pt-2 pokemon-img" 
      :alt="pokemon.name"
    >
    <div class="card-body">
      <h5 class="card-title text-center">{{ pokemon.name }}</h5>
      <hr>
      <div class="row">
        <section class="col">
          <strong>XP: </strong>
          <span>{{ pokemon.xp }}</span>
        </section>
        <section class="col">
          <strong>Altura: </strong>
          <span>{{ pokemon.height }}</span>
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.pokemon-img {
  height: 250px;
  padding-top: 2px;
}

.cardPokemonSelected {
  height: 450px;
  background: rgb(72,63,251);
  background: radial-gradient(circle, rgba(220, 194, 106, 0.8) 0%, rgba(244, 0, 0, 0.8) 100%);
}
</style>
