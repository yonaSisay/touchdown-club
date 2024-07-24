<script setup>
import { ref } from "vue";
const images = ref([
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
  "~/assets/temp/temp1.png",
]);
</script>

<template>
  <div>
    <div class="score-container">
      <div>
        <h1>
          2023 Football <br />
          Schedule & Scores
        </h1>
        <div>
          <UI-Score isScore v-for="i in 5" :key="i" />
          <UI-Score v-for="i in 5" :key="i" />
        </div>
      </div>
      <div class="wave"></div>
    </div>
    <div class="image-carousel">
      <img
        v-for="(image, i) in images"
        :key="i"
        src="~/assets/temp/temp1.png"
        alt="images"
      />
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "~/assets/css/landing/score-schedule";
</style>
