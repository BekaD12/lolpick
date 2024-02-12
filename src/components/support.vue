<script setup>
const champions = [
  { name: 'Maokai', tier: 'Main' },
  { name: 'Zyra', tier: 'Main' },
  { name: 'Leona', tier: 'Situational' },
  { name: 'Blitzcrank', tier: 'Situational' },
  { name: 'Lux', tier: 'Pressure' },
  { name: 'Xerath', tier: 'Pressure' },
  { name: 'Senna', tier: 'Pressure' },
  { name: 'Brand', tier: 'Pressure' },
  { name: 'Karma', tier: 'Enchanter' },
  { name: 'Renata', tier: 'Enchanter' },
]

const imgBaseUrl = 'https://opgg-static.akamaized.net/meta/images/lol/14.3.1/champion/'
const uggBaseUrl = 'https://u.gg/lol/champions/'
const opggBaseUrl = 'https://www.op.gg/champions/'

const generateImageUrl = name => `${imgBaseUrl}${name}.png`
const generateUggUrl = name => `${uggBaseUrl}${name}/build?role=adc`
const generateOpggUrl = name => `${opggBaseUrl}${name}/adc/build?`

const groupedChampions = champions.reduce((acc, champion) => {
  acc[champion.tier] ??= []
  acc[champion.tier].push({
    name: champion.name,
    displayName: champion.displayName || champion.name,
    image: generateImageUrl(champion.name),
    uggUrl: generateUggUrl(champion.name),
    opggUrl: generateOpggUrl(champion.name),
  })
  return acc
}, {})

const tiersWithChampions = Object.entries(groupedChampions).map(([tier, champions]) => ({
  title: tier,
  champions,
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
