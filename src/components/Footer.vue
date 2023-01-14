<script setup lang="ts">
import { isDark, toggleDark } from '~/composables'
</script>

<template>
  <nav flex justify-center p10>
    <button class="icon-btn !outline-none m-2" @click="toggleDark()">
      <div v-if="isDark" i-carbon-moon />
      <div v-else i-carbon-sun />
    </button>

    <button class="icon-btn !outline-none m-3" w="8">
      <a href="https://u.gg/lol/profile/euw1/bekad12/champion-stats?role=adc" target="_blank">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
          <g fill="none" fill-rule="evenodd">
            <path fill="#7878B5" d="M10.133 5.867H5.867v4.266h4.266z"></path>
            <path fill="#7878B5" d="M0 0v14.75l2.828-2.829V2.828h9.094L14.75 0z"></path>
            <path fill="var(--button)" d="M16 16V1.25L13.172 4.08v9.093H4.078L1.25 16z"></path>
          </g>
        </svg>
      </a>
    </button>

    <button class="icon-btn !outline-none m-3" w="8">
      <a href="https://u.gg/lol/profile/euw1/arsoniq/champion-stats?role=support" target="_blank">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
          <path d="M8.43 5.67l1.703 8.616L8 16l-2.133-1.714L7.57 5.67 8 6.249l.43-.578zM16 3.404c-.304 2.498-4.119
            2.261-4.119 2.261l1.75 2.315-2.81 1.13L9.6 5.234l1.857-1.83zm-11.457 0L6.4 5.233 5.18 9.11 2.368
            7.98l1.75-2.316S.305 5.901 0 3.403h4.543zM9.998 0l.669 1.185L8 4.456 5.333 1.185 6.003 0h3.995z"
            fill="var(--button)" fill-rule="evenodd">
          </path>
        </svg>
      </a>
    </button>
  </nav>
</template>
