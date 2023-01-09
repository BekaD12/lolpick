<script setup>

const synergie1 = ["Ashe", "Thresh"];
const synergie2 = ["Ezreal", "Karma"];
const synergie3 = ["Sivir", "Leona"];
const synergie4 = ["Kaisa", "Nautilus"];
const synergie5 = ["Caitlyn", "Lux"];

function link(i) {
  return 'https://u.gg/lol/champions/' + i + '/build'
}

function img(i) {
  return 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/' + i + '.webp'
}
</script>


<template>

  <div class="wrapper">

    <span class="role">Synergie</span>
    <div class="data">
      <div class="champion">
        <div v-for="i in synergie1" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <div class="champion">
        <div v-for="i in synergie2" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <div class="champion">
        <div v-for="i in synergie3" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <div class="champion">
        <div v-for="i in synergie4" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

    <div class="data">
      <div class="champion">
        <div v-for="i in synergie5" :key="i">
          <a :href="link(i)" target="blank">
            <img :src="img(i)">
          </a>
          <span class="name">{{ i }}</span>
        </div>
      </div>
    </div>

  </div>
</template>
