<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"]);
</script>

<template>
  <div class="col-4">
    <div class="card p-2 mb-3 cardListPokemon">
        <p class="text-center">{{ pokemon.name }}</p>
        <img 
        :src="urlBaseSvg" 
        class="card-img-top" 
        alt="..."
        height="80">
    </div>
  </div>
</template>

<style scoped>
.cardListPokemon {
  background: rgb(63,94,251);
  background: radial-gradient(circle, rgba(63,94,251,0.5) 0%, rgba(70,252,244,0.3) 100%);
  cursor: pointer;
}

.cardListPokemon:hover {
  background: rgb(63,94,251);
  background: radial-gradient(circle, rgba(63,94,251,0.7) 0%, rgba(70,252,244,0.5) 100%);
}

.cardListPokemon img:hover {
  padding: .1rem;
}
</style>