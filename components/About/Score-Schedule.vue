<script setup>
import { ref } from "vue";
const images = ref([
  "https://deep-image.ai/_next/static/media/app-info-generator.bf08e63e.webp",
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
          The touchdown club is a platform to fundraise for the school football
          <br />
          program.
        </h1>
        <div class="flex-col-center">
          <div class="description-card">
            There are two parts to the touchdown club: the offense and defense.
          </div>
          <div class="description-card">
            If a donor wants to contribute to the offense part of the touchdown
            club, they will agree to pay a sum of money each time the school
            scores a touchdown.
          </div>
          <div class="description-card">
            The touchdown club is very similar to a fundraising jog-a-thon. Each
            time a person runs a lap around the track, a donor agrees to pay a
            specific fee for each lap.
          </div>
          <div class="description-card">
            The most touchdowns the offense/defense can score is 8-touchdowns
            because of the below-defense touchdown system and to cap a donor
            financial generosity.
          </div>
          <div class="description-card">
            If a donor chooses to contribute to the defensive part of the
            touchdown club, a donor will agree to pay a sum by not allowing the
            opposing team to score. If the defense holds a team scoreless, it is
            like the offense scoring eight touchdowns or 56 points. For example,
            if a team scores three touchdowns, 21 points is minus 56 points, for
            a total of 35 points, which is five touchdowns. The donor would be
            responsible for paying the school defense for five touchdowns.
          </div>
          <div class="description-card">
            Read the Touchdown Club <span>Terms-and-conditions.</span>
          </div>

          <Auth-SignUp />
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
@import "~/assets/css/variables";

.score-container {
  z-index: 40;
  height: 1000px;
  margin-top: 300px;
  position: relative;
  padding: 30px 60px;
  display: flex;
  justify-content: center;
  overflow-x: visible;
}
h1 {
  font-weight: 700;
  color: white;
  font-size: 24px;
  line-height: 28px;
  text-align: center;
  font-family: Goldman;
}

.description-card {
  width: 800px;
  background: #242424;
  color: white;
  padding: 12px 24px;
  margin-top: 16px;
  span {
    color: $TDC-orange;
    border-bottom: 1px solid $TDC-orange;
  }
}

.wave {
  background-image: url("@/public/images/wave-background.png");
  background-size: cover;
  background-repeat: no-repeat;
  position: absolute;
  bottom: -280px;
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
  margin-top: 2px;
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
