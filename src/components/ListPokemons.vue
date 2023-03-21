<script setup>
const pokemon = defineProps(["name"]);
</script>

<template>
  <div>
    <div class="card">
        <p>{{ pokemon.name }}</p>
    </div>
  </div>
</template>