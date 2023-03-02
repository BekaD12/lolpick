<script setup>
const engage = ["Thresh", "Taric", "Amumu", "Nautilus", "Blitzcrank"];
const pressure = ["Ashe", "Senna", "Morgana", "Zyra", "Lux"];
const enchanter = ["Karma", "Seraphine"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build?role=support'
}

function opgg(i) {
  return 'https://www.op.gg/champions/' + i + '/support/build?region=global&tier=platinum_plus'
}

function img(i) {
  return 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/' + i + '.webp'
}
</script>


<template>
  <div class="wrapper">
    <span class="role">support</span>

    <span class="tier">Engage</span>
    <div class="data">
      <div class="card" v-for="i in engage" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Pressure</span>
    <div class="data">
      <div class="card" v-for="i in pressure" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <a :href="opgg(i)" title="op.gg" target="_blank">
          <span class="name">{{ i }}</span>
        </a>
      </div>
    </div>

    <span class="tier">Enchanter</span>
    <div class="data">
      <div class="card" v-for="i in enchanter" :key="i">
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
