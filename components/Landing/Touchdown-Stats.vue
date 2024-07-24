import PlayerRosterBio from '../Player-Roster-Bio.vue';
<template>
  <div>
    <div class="blue">
      <h3>touchd<span></span>wn club</h3>
      <div class="grid-cols-2">
        <div class="left-column">
          <img
            src="@/assets/images/central-catholic.png"
            alt="central catholic logo"
          />
          <div class="stats-container">
            <div class="grid-cols-3">
              <div></div>
              <h1 class="text-center">TOTAL TOUCHDOWNS</h1>
              <h1 class="text-center">TOTAL MONEY DONATED</h1>
            </div>
            <div class="grid-cols-3">
              <div>Defense</div>
              <h2 class="text-center">100</h2>
              <h2 class="text-center">$5,000</h2>
            </div>
            <div class="grid-cols-3">
              <div>Offense</div>
              <h2 class="text-center">100</h2>
              <h2 class="text-center">$5,000</h2>
            </div>
          </div>
          <ul>
            <PlayerRosterBio />
            <li>Coaches Bio <Icon icon="lucide:chevrons-right" /></li>
            <li>
              2023 Offense Statistics <Icon icon="lucide:chevrons-right" />
            </li>
            <li>
              2023 Defensive Statistics <Icon icon="lucide:chevrons-right" />
            </li>
          </ul>
        </div>
        <div class="right-column">
          <UI-CircleStats />
        </div>
      </div>
    </div>
    <img class="player-image" src="@/assets/images/player.png" alt="player" />
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/css/landing/touchdown-stats";
</style>
