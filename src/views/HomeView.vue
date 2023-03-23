<script setup>
import { onMounted, reactive, ref, computed } from 'vue';
import ListPokemons from '../components/ListPokemons.vue';

let urlBaseSvg = ref("https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/");
let pokemons = reactive(ref());
let searchPokemonField = ref("");

onMounted(() => {
  fetch("https://pokeapi.co/api/v2/pokemon?limit=151&offset=0")
    .then(res => res.json())
    .then(res => pokemons = res.results);
});

const pokemonsFiltered = computed(() => {
  if(pokemons.value && searchPokemonField.value){
    return pokemons.value.filter(pokemon => 
      pokemon.name.toLowerCase().includes(searchPokemonField.value.toLowerCase())
    );
  }
  return pokemons.value;
});

</script>

<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-6">
          <div class="card" style="width: 18rem;">
            <img src="https://t2.tudocdn.net/301383?w=1920" class="card-img-top" alt="...">
            <div class="card-body">
              <h5 class="card-title">Card title</h5>
              <p class="card-text">
                Some quick example text to build on the card title and make up the bulk of the card's content.
              </p>
            </div>
          </div>
        </div>
        <div class="col-sm-12 col-md-6">
            <div class="card">
              <div class="card-body row">

                <div class="mb-3">
                  <label 
                    hidden 
                    for="searchPokemonField" 
                    class="form-label">
                      Pesquisar...
                  </label>

                  <input 
                    v-model="searchPokemonField"
                    type="text" 
                    class="form-control" 
                    id="searchPokemonField" 
                    placeholder="Pesquisar..."
                  >
                </div>

                <ListPokemons
                v-for="pokemon in pokemonsFiltered"
                :key="pokemon.name"
                :name="pokemon.name"
                :urlBaseSvg="urlBaseSvg + pokemon.url.split('/')[6] + '.svg'" 
                />
              </div>
            </div>
          </div>
      </div>
    </div>
  </main>
</template>
