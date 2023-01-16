<script setup>

const synergie1 = ["Sivir", "Leona"];
const synergie2 = ["Draven", "Thresh"];
const synergie3 = ["Ezreal", "Karma"];
const synergie4 = ["Kaisa", "Nautilus"];
const synergie5 = ["Caitlyn", "Lux"];
const synergie6 = ["Samira", "Rell"];
const synergie7 = ["Seraphine", "Senna"];

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
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie2" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie3" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie4" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie5" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie6" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

    <div class="data">
      <div class="card" v-for="i in synergie7" :key="i">
        <a :href="link(i)" target="blank">
          <img :src="img(i)">
        </a>
        <span class="name">{{ i }}</span>
      </div>
    </div>

  </div>
</template>
