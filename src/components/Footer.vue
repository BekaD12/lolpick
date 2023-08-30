<script setup lang="ts">
</script>

<template>
  <nav flex justify-center p10>
    <button class="m-4 w-8 icon-btn !outline-none" title="Toggle dark mode" @click="toggleDark()">
      <div v-if="isDark" i-carbon-moon />
      <div v-else i-carbon-sun />
    </button>

    <button class="m-4 w-8 icon-btn !outline-none">
      <a href="https://www.leagueoflegends.com/fr-fr/news/game-updates/" target="_blank" title="Patch notes & Updates">
        <div i-carbon:update-now />
      </a>
    </button>

    <button class="m-4 w-7 icon-btn !outline-none">
      <a href="https://u.gg/lol/adc-tier-list" target="_blank" title="u.gg ADC tier list">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
          <g fill="none" fill-rule="evenodd">
            <path fill="#7878B5" d="M10.133 5.867H5.867v4.266h4.266z" />
            <path fill="#7878B5" d="M0 0v14.75l2.828-2.829V2.828h9.094L14.75 0z" />
            <path fill="var(--button)" d="M16 16V1.25L13.172 4.08v9.093H4.078L1.25 16z" />
          </g>
        </svg>
      </a>
    </button>

    <button class="m-4 w-7 icon-btn !outline-none">
      <a href="https://u.gg/lol/support-tier-list" target="_blank" title="u.gg Support tier list">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16">
          <path
            d="M8.43 5.67l1.703 8.616L8 16l-2.133-1.714L7.57 5.67 8 6.249l.43-.578zM16 3.404c-.304 2.498-4.119
            2.261-4.119 2.261l1.75 2.315-2.81 1.13L9.6 5.234l1.857-1.83zm-11.457 0L6.4 5.233 5.18 9.11 2.368
            7.98l1.75-2.316S.305 5.901 0 3.403h4.543zM9.998 0l.669 1.185L8 4.456 5.333 1.185 6.003 0h3.995z"
            fill="var(--button)" fill-rule="evenodd"
          />
        </svg>
      </a>
    </button>
  </nav>
</template>
