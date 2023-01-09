<script setup lang="ts">
import { isDark, toggleDark } from '~/composables'
</script>

<template>
  <nav flex justify-center p10>
    <button class="icon-btn !outline-none" @click="toggleDark()">
      <div v-if="isDark" i-carbon-moon />
      <div v-else i-carbon-sun />
    </button>
  </nav>
</template>
