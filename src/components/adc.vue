<script setup>

const tier1 = ["Ezreal", "Sivir", "Ashe"];
const tier2 = ["Kaisa", "Draven", "Caitlyn"];
const tier3 = ["Seraphine", "Ziggs"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build?role=adc'
}

function img(i) {
  return 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/' + i + '.webp'
}
</script>

<template>
  <div class="wrapper">
    <span class="role">adc</span>

    <span class="tier">Tier 1</span>
    <div class="data">
      <div class="card" v-for="i in tier1" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <span class="tier">Tier 2</span>
    <div class="data">
      <div class="card" v-for="i in tier2" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <span class="tier">Tier 3</span>
    <div class="data">
      <div class="card" v-for="i in tier3" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

  </div>
</template>
