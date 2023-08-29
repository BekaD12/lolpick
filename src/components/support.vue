<script setup>
const champions = [
  { name: 'Thresh', tier: 'Main' },
  { name: 'Leona', tier: 'Main' },
  { name: 'Nautilus', tier: 'Main' },
  { name: 'Blitzcrank', tier: 'Main' },
  { name: 'Rell', tier: 'Situational' },
  { name: 'Taric', tier: 'Situational' },
  { name: 'Xerath', tier: 'Pressure' },
  { name: 'Senna', tier: 'Pressure' },
  { name: 'Karma', tier: 'Enchanter' },
]

const tiers = [
  { title: 'Main', champions: [] },
  { title: 'Situational', champions: [] },
  { title: 'Pressure', champions: [] },
  { title: 'Enchanter', champions: [] },
]

const imgBaseUrl = 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/'
const uggBaseUrl = 'https://u.gg/lol/champions/'
const opggBaseUrl = 'https://www.op.gg/champions/'

const generateImageUrl = name => `${imgBaseUrl}${name}.webp`
const generateUggUrl = name => `${uggBaseUrl}${name}/build?role=suppport`
const generateOpggUrl = name => `${opggBaseUrl}${name}/suppport/build?region=global&tier=platinum_plus`

const tiersWithChampions = tiers.map(tier => ({
  ...tier,
  champions: champions.filter(champion => champion.tier === tier.title)
    .map(champion => ({
      name: champion.name,
      image: generateImageUrl(champion.name),
      uggUrl: generateUggUrl(champion.name),
      opggUrl: generateOpggUrl(champion.name),
    })),
}))
</script>

<template>
  <div class="wrapper">
    <span class="role">support</span>
    <div v-for="tierData in tiersWithChampions" :key="tierData.title" class="tier">
      <span class="tier">{{ tierData.title }}</span>
      <div class="data">
        <ChampionCard v-for="champion in tierData.champions" :key="champion.name" :champion="champion" />
      </div>
    </div>
  </div>
</template>
