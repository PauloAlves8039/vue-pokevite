<template>
  <div class="about">
    <div class="container mt-4 text-body-secondary">
      <div class="card" style="margin-bottom: 100px">
        <h1 class="text-center">PokeVite</h1>
        <div class="card-body">
          <h2>Objetivo:</h2>
          <p>Esse é mais um projeto desenvolvido para fins didáticos com intúito de praticar o desenvolvimento com Vue 3
            utilizando Vite e consumindo a API PokeAPI.</p>
          <hr>
          <h3>Recursos Utilizados</h3>
          <ul>
            <li>
              <a href="https://vitejs.dev/guide/" target="_blank" alt="CSS 3">Vite</a> 
            </li>
            <li>
              <a href="https://vuejs.org/" target="_blank" alt="Vue.js 3">Vue.js 3</a> 
            </li>
            <li>
              <a href="https://router.vuejs.org/" target="_blank" alt="Vue Router">Vue Router</a> 
            </li>
            <li>
              <a href="https://getbootstrap.com/docs/5.0/getting-started/introduction/" target="_blank" alt="Bootstrap 5">Bootstrap 5</a> 
            </li>
            <li>
              <a href="https://animate.style/" target="_blank" alt="Animate CSS">Animate CSS</a> 
            </li>
            <li>
              <a href="https://pokeapi.co/" target="_blank" alt="PokeAPI">PokeAPI</a> 
            </li>
          </ul>
          <p>
            Repositório do Projeto: <a href="https://github.com/PauloAlves8039/vue-pokevite" target="_blank" alt="Link do projeto no GitHub">PokeVite</a>
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

h1 {
  color: rgb(63,94,251);
}
</style>
