<script setup>
const champions = [
  { name: 'Sivir', tier: 'Main' },
  { name: 'Ezreal', tier: 'Main' },
  { name: 'Kaisa', tier: 'Main' },
  { name: 'Ashe', tier: 'Main' },
  { name: 'Draven', tier: 'Situational' },
  { name: 'Nilah', tier: 'Situational' },
  { name: 'Caitlyn', tier: 'Situational' },
  { name: 'Xayah', tier: 'Situational' },
  { name: 'Seraphine', tier: 'APC' },
  { name: 'Ziggs', tier: 'APC' },
  { name: 'Varus', tier: 'Lethality' },
  { name: 'MissFortune', tier: 'Lethality', displayName: 'MF' },
]

const tiers = [
  { title: 'Main', champions: [] },
  { title: 'Situational', champions: [] },
  { title: 'APC', champions: [] },
  { title: 'Lethality', champions: [] },
]

const imgBaseUrl = 'https://static.bigbrain.gg/assets/lol/riot_static/12.23.1/img/champion/'
const uggBaseUrl = 'https://u.gg/lol/champions/'
const opggBaseUrl = 'https://www.op.gg/champions/'

const generateImageUrl = name => `${imgBaseUrl}${name}.webp`
const generateUggUrl = name => `${uggBaseUrl}${name}/build?role=adc`
const generateOpggUrl = name => `${opggBaseUrl}${name}/adc/build?region=global&tier=platinum_plus`

const tiersWithChampions = tiers.map(tier => ({
  ...tier,
  champions: champions.filter(champion => champion.tier === tier.title)
    .map(champion => ({
      name: champion.name,
      displayName: champion.displayName,
      image: generateImageUrl(champion.name),
      uggUrl: generateUggUrl(champion.name),
      opggUrl: generateOpggUrl(champion.name),
    })),
}))
</script>

<template>
  <div class="wrapper">
    <span class="role">adc</span>
    <div v-for="tierData in tiersWithChampions" :key="tierData.title" class="tier">
      <span class="tier">{{ tierData.title }}</span>
      <div class="data">
        <ChampionCard v-for="champion in tierData.champions" :key="champion.name" :champion="champion" />
      </div>
    </div>
  </div>
</template>
