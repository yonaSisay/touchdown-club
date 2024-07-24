<template>
  <div class="body">
    <b-row>
      <b-col>
        <b-row
          ><div class="img-container">
            <img src="~/assets/belle 1.png" alt="" />
          </div>
          <div class="small-card background-black">
            <p>BELLEVUE</p>
            <h4>Away <span class="dot"></span> Non-Disctrict</h4>
          </div>
        </b-row>
        <b-row class="mt-2"
          ><div class="img-container">
            <img src="~/assets/jesuit.png" alt="" />
          </div>
          <div class="small-card background-black">
            <p>jesuit <span>portland</span></p>
            <h4>
              Away
              <span class="dot"></span>
              Non-League
            </h4>
          </div>
        </b-row>
      </b-col>

      <b-col class="flex-col-center">
        <h2>
          laying <br />
          bricks
        </h2>
      </b-col>
    </b-row>

    <!-- Second Row -->

    <b-row class="mt-5">
      <b-col>
        <b-row class="mt-2" v-for="i in 3" :key="i"
          ><div class="img-container">
            <img src="~/assets/sandy.png" alt="" />
          </div>
          <div class="small-card background-orange">
            <p>sandy</p>
            <h4>Away <span class="dot"></span> Non-Disctrict</h4>
          </div>
        </b-row>
        <b-row v-for="i in 3" :key="i" class="mt-2"
          ><div class="img-container">
            <img src="~/assets/nelson.png" alt="" />
          </div>
          <div class="small-card background-orange">
            <p>nelson <span>happy valley</span></p>
            <h4>
              Away
              <span class="dot"></span>
              Non-League
            </h4>
          </div>
        </b-row>
      </b-col>

      <b-col class="flex-col-center">
        <h2>
          ram
          <br />
          pride
        </h2>
      </b-col>
    </b-row>

    <!-- Third Row -->
    <b-row class="mt-5">
      <b-col>
        <b-row
          ><div class="img-container"></div>
          <div class="small-card background-red">
            <p>play-off game</p>
          </div>
        </b-row>
        <b-row v-for="i in 3" :key="i" class="mt-2"
          ><div class="img-container"></div>
          <div class="small-card background-red"><p>quarter-finals</p></div>
        </b-row>
      </b-col>

      <b-col class="flex-col-center">
        <h2>
          championships <br />
          are won in <br />
          november
        </h2>
      </b-col>
    </b-row>
  </div>
</template>

<style scoped lang="scss">
@import "~/assets/css/cc-schedule/body";
</style>
