import PlayerRosterBio from '../Player-Roster-Bio.vue';
<template>
  <div>
    <div class="blue">
      <h3>touchd<span></span>wn club</h3>
      <div class="grid-cols-2">
        <div class="left-column">
          <img
            src="@/public/images/central-catholic.png"
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
    <img class="player-image" src="@/public/images/player.png" alt="player" />
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";

.blue {
  height: 1034px;
  background-color: $blue;
  clip-path: polygon(0% 0%, 100% 20%, 100% 70%, 0% 100%);
  width: 100%;
  position: absolute;
  z-index: 50;
  top: 760px;
  color: white;
  padding: 0 60px;
  padding-top: 140px;
  h3 {
    font-size: 1rem;
    display: flex;
    align-items: center;
    gap: 2px;
    margin-bottom: 2rem;
    span {
      background: $TDC-orange;
      width: 1rem;
      height: 1rem;
      display: inline-block;
      border-radius: 50%;
    }
  }
}

.grid-cols-2 {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 10px;
}

.left-column {
  display: flex;
  flex-direction: column;
  gap: 60px;
  ul {
    list-style-type: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 30px;

    li {
      font-size: 20px;
      line-height: 24px;
      font-weight: 400;
      font-family: Goldman;
    }
  }
  img {
    width: 466px;
    height: 96px;
  }
}

.stats-container {
  width: 668px;
  height: 218px;
  background-color: rgba(255, 255, 255, 0.15);
  display: flex;
  flex-direction: column;
  justify-content: center;
  border-radius: 2px;
  border: 4px solid #779791;
  padding: 30px 20px;
}

.grid-cols-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  margin-top: 20px;
  h2 {
    font-size: 40px;
    line-height: 48px;
    font-family: Goldman;
  }
  h1 {
    font-size: 12px;
    line-height: 14.52px;
    font-weight: 400;
  }
}

.player-image {
  position: absolute;
  top: 1160px;
  left: 900px;
  z-index: 100;
  width: 326px;
}
</style>
