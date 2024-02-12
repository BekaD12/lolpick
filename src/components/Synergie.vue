<script setup>
const synergies = [
  ['Seraphine', 'Senna'],
  ['Ezreal', 'Karma'],
  ['Caitlyn', 'Lux'],
]

function img(champion) {
  return `https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/${champion}.webp`
}
</script>

<template>
  <div class="wrapper">
    <span class="role">synergie</span>
    <div v-for="(synergy, index) in synergies" :key="index" class="data">
      <div v-for="champion in synergy" :key="champion" class="card">
        <img :src="img(champion)" :alt="`${champion} Icon`">
        <span class="name">{{ champion }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.role{
  margin-bottom: 5rem;
}
</style>
