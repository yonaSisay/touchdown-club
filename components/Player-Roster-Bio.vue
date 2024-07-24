<script setup>
import { ref } from "vue";
</script>

<template>
  <div>
    <li v-b-modal.roasterBio>
      Player Roster/Bio <Icon icon="lucide:chevrons-right" />
    </li>
    <b-modal id="roasterBio" hide-footer size="xl">
      <template #modal-title>Player Roster/Bio </template>
      <b-col>
        <h1 class="main-title">Central Catholic High School Roster</h1>
        <b-row cols="4">
          <b-col class="mt-2" v-for="i in 8" :key="i">
            <img src="~/assets/Rectangle 20.png" alt="images" />
          </b-col>
        </b-row>
      </b-col>
      <div class="flex-between">
        <span></span>
        <button class="orange-button">Okay</button>
      </div>
    </b-modal>
  </div>
</template>

<style scoped lang="scss">
ul {
  list-style-type: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 30px;

  li {
    font-size: 20px;
    line-height: 24px;
    font-weight: 400;
    font-family: Goldman;
  }
}
</style>
