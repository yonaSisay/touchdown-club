<template>
  <div class="outer_circle">
    <div class="inner_circle"></div>
    <div class="circle-content">
      <h2>$10,000</h2>
      <p>Total Money Donated</p>
    </div>
  </div>
</template>

<style lang="scss">
@import "@/assets/css/variables";

.outer_circle {
  position: relative;
  margin: 50px;
  margin-left: 220px;
  width: 484px;
  height: 484px;
  border-radius: 50%;
  background: $blue;
  padding: 25px;
}

.inner_circle {
  background-image: linear-gradient(
    to bottom,
    #f07707 -16.45%,
    #dda775 48.61%,
    #c46812 124.32%
  );
  position: absolute;
  top: -10px;
  bottom: -10px;
  right: -10px;
  left: -10px;
  z-index: -1;
  border-radius: inherit;
}

.circle-content {
  width: 100%;
  height: 100%;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.15);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  h2 {
    font-family: Goldman;
    font-weight: 700;
    font-size: 80px;
    line-height: 96px;
  }
  p {
    font-size: 18px;
    line-height: 21.78px;
    font-weight: 400;
    text-align: center;
  }
}
</style>
