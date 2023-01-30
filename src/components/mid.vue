<script setup>

const tier1 = ["Lux", "Lissandra", "Ahri"];
const tier2 = ["TwistedFate", "Malzahar", "Viktor"];
const tier3 = ["Zilean", "Rumble", "Seraphine"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build?role=top'
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
    <span class="role">mid</span>

    <span class="tier">Main</span>
    <div class="data">
      <div class="card" v-for="i in tier1" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)" loading="lazy">
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
          <span class="name">{{ i.replace("TwistedFate", "TF") }}</span>
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
