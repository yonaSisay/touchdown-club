import PlayerRosterBio from '../Player-Roster-Bio.vue';
<template>
  <div class="blue"></div>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";

.blue {
  height: 555px;
  background-color: $blue;
  clip-path: polygon(0% 0%, 100% 40%, 100% 100%, 0% 100%);
  width: 100%;
  position: absolute;
  z-index: 50;
  top: 760px;
  color: white;
  padding: 0 60px;
  padding-top: 140px;
}
</style>
