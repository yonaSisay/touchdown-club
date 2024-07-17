<script>
export default {};
</script>
<template>
  <div class="container">
    <TopNav />
    <Auth-VerifyEmail />
    <!-- Hero page section -->
    <div class="hero">
      <h1>
        Join the <br />
        Touchdown Club
      </h1>
      <h2>
        Fueling dreams, powering victories for our school <br />
        football program!
      </h2>

      <Auth-SignUp />
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
  h2 {
    line-height: 36px;
    font-size: 18px;
    font-weight: 400;
    text-align: center;
  }
}
</style>
