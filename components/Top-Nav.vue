<script>
export default {
  name: "IndexPage",
};
</script>

<template>
  <nav>
    <h1>touchd<span></span> wn club</h1>
    <ul>
      <li v-for="i in 4" :key="i">Menu {{ i }}</li>
    </ul>
    <Auth-Login />
  </nav>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";

nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  h1 {
    font-size: 1.5rem;
    display: flex;
    align-items: center;
    gap: 2px;
    span {
      background: $TDC-orange;
      width: 1.2rem;
      height: 1.2rem;
      display: inline-block;
      border-radius: 50%;
    }
  }

  ul {
    display: flex;
    gap: 4rem;
    margin: 0;
    padding: 0;
    list-style: none;
  }
}

.custom-button {
  padding: 7px 30px;
}
</style>
