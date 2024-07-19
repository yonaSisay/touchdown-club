<script setup>
import { ref } from "vue";
const currentStep = ref(1);
</script>

<template>
  <div>
    <button v-b-modal.emailVerified>setup Account</button>
    <b-modal
      id="emailVerified"
      hide-header
      hide-footer
      modal-class="custom-modal"
    >
      <b-col cols="12" class="content">
        <h2>Setup account<span></span></h2>
        <p class="sub-title-p">
          Last steps before you become a member of the club! Introduce yourself.
        </p>
        <SetupAccountStepper :currentStep="currentStep" />
        <SetupAccountYourTeam v-if="currentStep == 1" />
        <SetupAccountPersonelInfo v-if="currentStep == 2" />
        <SetupAccountPayment v-if="currentStep == 3" />
        <div class="flex-between border-top">
          <button
            v-if="currentStep > 1"
            class="white-button"
            @click="currentStep--"
          >
            Back
          </button>
          <span v-else></span>

          <button
            class="orange-button"
            @click="currentStep++"
            :disabled="currentStep == 3"
          >
            Next
          </button>
        </div>
      </b-col>
    </b-modal>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";
.border-top {
  border-top: $extra-light;
  margin-top: 3rem;
}
h2 {
  font-family: Goldman;
  font-size: 24px;
  line-height: 28px;
  display: flex;
  align-items: center;
  gap: 5px;
  text-align: start;
  span {
    background: $TDC-orange;
    width: 1.2rem;
    height: 1.2rem;
    display: inline-block;
    border-radius: 50%;
  }
}

.content {
  padding: 20px;
}

.sub-title-p {
  font-family: Inter;
  font-size: 14px;
  line-height: 21px;
  font-weight: 400;
  color: $light-gray;
}
</style>
