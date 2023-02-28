<script setup>
const tier1 = ["Sivir", "Kaisa", "Xayah"];
const tier2 = ["Nilah", "Draven", "Caitlyn", "MissFortune"];
const tier3 = ["Seraphine", "Ziggs", "Senna", "Ezreal"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build?role=adc'
}

function opgg(i) {
  return 'https://www.op.gg/champions/' + i + '/adc/build?region=global&tier=platinum_plus'
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
        <a :href="link(i)" target="_blank" title="u.gg">
          <img :src="img(i)">
        </a>

        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Situational</span>
    <div class="data">
      <div class="card" v-for="i in tier2" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i.replace("MissFortune", "MF") }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Pocket pick</span>
    <div class="data">
      <div class="card" v-for="i in tier3" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

  </div>
</template>
