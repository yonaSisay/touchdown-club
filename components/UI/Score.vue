<script setup>
const props = defineProps({
  isScore: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <div class="schedule-score">
    <div class="team-name text-end"><span>Central Catholic HS</span></div>
    <div class="team-score">
      <img src="@/public/images/central-logo.png" alt="central logo" />
      <div :class="isScore ? '' : 'is-schedule'">
        {{ isScore ? "12 - 0" : "N/A" }}
      </div>
      <img src="@/public/images/east-logo.png" alt="east logo" />
    </div>
    <div class="team-name text-start"><span>EAST Catholic HS</span></div>
  </div>
</template>

<style lang="scss">
@import "@/assets/css/variables";

.schedule-score {
  width: 1451px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 43px;

  font-size: 24px;
  line-height: 28.8px;
  font-weight: 400;
  font-family: Goldman;
  color: white;
  margin-top: 24px;
  z-index: 50;
}
.team-name {
  width: 520px;
  height: 53px;
  background: #242424;
  padding: 12px 24px;
}

.text-end {
  text-align: end;
}
.text-start {
  text-align: start;
}

.is-schedule {
  background: rgba(36, 36, 36, 1) !important;
}

.team-score {
  display: flex;
  height: 53px;
  justify-content: center;
  gap: 53px;

  div {
    background: $TDC-orange;
    width: 133px;
    text-align: center;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 32px;
    font-weight: 700;
  }

  img {
    width: 53px;
  }
}
</style>
