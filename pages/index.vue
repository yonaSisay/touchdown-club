<script>
export default {
  name: "IndexPage",
};
</script>
<template>
  <div class="container-fluid">
    <!-- Hero section -->
    <Landing-Hero />
    <!-- Touchdown stats section-->
    <Landing-TouchdownStats />
    <!-- schedule and score -->
    <Landing-ScoreSchedule />
  </div>
</template>

<style lang="scss">
@import "./../assets/css/variables";
</style>
