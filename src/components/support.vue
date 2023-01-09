<script setup>

const tier1 = ["Thresh", "Nautilus", "Leona"];
const tier2 = ["Karma", "Blitzcrank", "Alistar"];
const tier3 = ["Taric", "Braum"];

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
    <div class="data">
      <h2>Tier 1</h2>
      <div class="champion">
        <div v-for="i in tier1" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <h2>Tier 2</h2>
      <div class="champion">
        <div v-for="i in tier2" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <h2>Tier 3</h2>
      <div class="champion">
        <div v-for="i in tier3" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

  </div>
</template>
