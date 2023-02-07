<script setup>

const synergie1 = ["Xayah", "Rakan"];
const synergie2 = ["Caitlyn", "Lux"];
const synergie3 = ["Sivir", "Taric"];
const synergie4 = ["Ezreal", "Karma"];
const synergie5 = ["Seraphine", "Ashe"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build'
}

function img(i) {
  return 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/' + i + '.webp'
}
</script>

<template>
  <div class="wrapper">
    <span class="role">synergie</span>

    <div class="data">
      <div class="card" v-for="i in synergie1" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie2" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie3" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie4" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie5" :key="i">
        <a :href="link(i)" target="_blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

  </div>
</template>
