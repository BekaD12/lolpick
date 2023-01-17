<script setup>

const tier1 = ["Ezreal", "Sivir", "Kaisa"];
const tier2 = ["Vayne", "Ashe", "Nilah", "Draven"];
const tier3 = ["Seraphine", "Ziggs", "Samira", "Caitlyn"];

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

    <span class="tier">Main</span>
    <div class="data">
      <div class="card" v-for="i in tier1" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <span class="tier">Situational</span>
    <div class="data">
      <div class="card" v-for="i in tier2" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <span class="tier">Pocket pick</span>
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
