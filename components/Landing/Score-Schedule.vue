<script setup>
import { ref } from "vue";
const images = ref([
  "https://deep-image.ai/_next/static/media/app-info-generator.bf08e63e.webp",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
  "../../assets/temp/temp1.png",
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
        src="../../assets/temp/temp1.png"
        alt="images"
      />
    </div>
  </div>
</template>

<style scoped lang="scss">
.score-container {
  z-index: 40;
  height: 1000px;
  margin-top: 700px;
  position: relative;
  padding: 30px 60px;
  display: flex;
  justify-content: center;
  overflow-x: visible;
}
h1 {
  font-weight: 700;
  color: white;
  font-size: 80px;
  line-height: 96px;
  text-align: center;
  font-family: Goldman;
}

.wave {
  background-image: url("@/assets/images/wave-background.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  bottom: -380px;
  left: 0;
  width: 100%;
  height: 70%;
  z-index: -2;
}

.image-carousel {
  display: flex;
  justify-content: center;
  overflow: auto;
  gap: 40px;
  width: 100%;
  z-index: 50;
  margin-top: 96px;
  padding-bottom: 40px;
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */

  &::-webkit-scrollbar {
    display: none; /* Chrome, Safari, Opera */
  }

  img {
    width: 400px;
    z-index: inherit;
  }
}
</style>
