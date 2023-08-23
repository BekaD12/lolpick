<script setup>

const tier1 = ['Shen', 'Zac']
const tier2 = ['Illaoi', 'Quinn']
const tier3 = ['Gwen', 'Jayce']

function link(i) {
  return `https://u.gg/lol/champions/${i}/build?role=top`
}

function opgg(i) {
  return `https://www.op.gg/champions/${i}/adc/build?region=global&tier=platinum_plus`
}

function img(i) {
  return `https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/${i}.webp`
}
</script>

<template>
  <div class="wrapper">
    <span class="role">top</span>

    <span class="tier">Main</span>
    <div class="data">
      <div v-for="i in tier1" :key="i" class="card">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Situational</span>
    <div class="data">
      <div v-for="i in tier2" :key="i" class="card">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Pocket pick</span>
    <div class="data">
      <div v-for="i in tier3" :key="i" class="card">
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
