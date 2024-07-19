<script setup>
import { ref } from "vue";
const isOffense = ref(true);
</script>
<template>
  <div class="content-wrapper">
    <b-col>
      <b-row>
        <h5><span class="star">*</span> Choose offense or defense</h5>
        <div class="flex-between">
          <button
            class="outline-button"
            @click="isOffense = true"
            :class="isOffense ? 'active-button' : ''"
          >
            Offense
          </button>
          <button
            class="outline-button"
            @click="isOffense = false"
            :class="isOffense ? '' : 'active-button'"
          >
            Defense
          </button>
        </div></b-row
      >

      <b-row class="mt-4">
        <h5>
          <span class="star">*</span> For every touchdown, how much are you
          going to give?
        </h5>
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="$0.00"
          class="custom-input"
        ></b-form-input>
      </b-row>

      <b-row v-if="isOffense" class="mt-4">
        <b-form-checkbox
          id="offense"
          name="offense"
          value="accepted"
          unchecked-value="not_accepted"
          class="checkbox"
        >
          I agree to pay this amount to the Touchdown Club for offense team.
        </b-form-checkbox></b-row
      >
      <b-row v-else class="mt-4">
        <b-form-checkbox
          id="defense"
          name="defense"
          value="accepted"
          unchecked-value="not_accepted"
          class="checkbox"
        >
          If a donor chooses to contribute to the defensive part of the
          touchdown club, a donor will agree to pay a sum by not allowing the
          opposing team to score. <span> Read more</span>
        </b-form-checkbox></b-row
      >
    </b-col>
  </div>
</template>
<style scoped lang="scss">
@import "@/assets/css/variables";

.outline-button {
  all: unset;
  border: 1px solid $TDC-orange;
  color: $TDC-orange;
  font-weight: 400;
  padding: 12px 30px;
  border-radius: 3px;
  width: 100%;
  text-align: center;
  cursor: pointer;
}

.active-button {
  background-color: $TDC-orange !important;
  color: white !important;
}

.content-wrapper {
  h5 {
    font-weight: 400;
    font-size: 14px;
    display: flex;
    align-items: center;
    gap: 5px;
  }
}
</style>
