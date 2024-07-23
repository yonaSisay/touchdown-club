<script>
export default {};
</script>
<template>
  <div class="container">
    <TopNav />

    <!-- Hero page section -->
    <div class="hero">
      <h1>About Us</h1>

      <Auth-SignUp />

      <img class="img" src="~/assets/aboutus.png" alt="image" />
    </div>
  </div>
</template>

<style lang="scss">
.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-top: 140px;
  h1 {
    font-weight: 700;
    font-size: 100px;
    line-height: 120px;
    text-align: center;
    font-family: Goldman;
  }
  img {
    position: absolute;
    bottom: -220px;
    z-index: 100;
  }
}
</style>
