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
.body {
  margin-top: 20px;
  width: 1000px;
  background: rgba(67, 0, 0, 0.9);
  color: white;
  padding: 120px 63px;
  box-shadow: 0px 10px 20px 0px rgba(0, 0, 0, 1);
}

.dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  display: inline-block;
}

.img-container {
  display: flex;
  align-items: center;
  width: 70px;
  img {
    object-fit: contain;
  }
}

.small-card {
  border-radius: 5px;
  padding: 12px 24px;
  width: 300px;
  margin-left: 20px;
  p {
    font-family: Goldman;
    font-weight: 400;
    font-size: 24px;
    line-height: 28.8px;
    text-transform: uppercase;
    white-space: nowrap;
    span {
      font-size: 18px !important;
    }
  }
  h4 {
    font-weight: 400;
    font-size: 14px;
    line-height: 16px;
    display: flex;
    align-items: center;
    gap: 0 8px;
  }
}

.background-black {
  color: white;
  background: black;
}

.background-orange {
  background: rgba(246, 207, 68, 1);
  color: black;
}

.background-red {
  background: rgba(164, 26, 69, 1);
  color: white;
}

h2 {
  font-weight: 700;
  font-size: 48px;
  line-height: 56px;
  text-align: center;
  font-family: Goldman;
  text-transform: uppercase;
}
</style>
