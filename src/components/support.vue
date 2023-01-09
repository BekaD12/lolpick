<script setup>

const tier1 = ["Thresh", "Nautilus", "Leona"];
const tier2 = ["Karma", "Lux", "Renata"];
const tier3 = ["Taric", "Brand", "Senna"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build?role=support'
}

function img(i) {
  return 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/' + i + '.webp'
}
</script>


<template>
  <div class="wrapper">
    <span class="role">support</span>

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
