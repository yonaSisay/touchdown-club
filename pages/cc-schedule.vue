<script>
export default {
  name: "IndexPage",
};
</script>
<template>
  <div class="cc-schedule-container">
    <div class="flex-col-center">
      <CcSchedule-Header />
      <CcSchedule-body />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.cc-schedule-container {
  height: 2231px;
  width: 100%;
  background-image: url("~/assets/cc-schedule-background.png");
}
</style>
