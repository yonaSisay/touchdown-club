<script setup>
const props = defineProps({
  currentStep: {
    type: Number,
    default: 1,
  },
});
</script>

<template>
  <div class="grid-cols-3">
    <div class="step" :class="currentStep == 1 ? 'active-step' : ''">
      <span>1</span>
      <div>
        <h4>Step 1</h4>
        <p>Your Team</p>
      </div>
      <Icon class="icon" icon="quill:chevron-right" />
    </div>
    <div class="step" :class="currentStep == 2 ? 'active-step' : ''">
      <span>2</span>
      <div>
        <h4>Step 2</h4>
        <p>Personal info</p>
      </div>
      <Icon class="icon" icon="quill:chevron-right" />
    </div>
    <div class="step" :class="currentStep == 3 ? 'active-step' : ''">
      <span>3</span>
      <div>
        <h4>Step 3</h4>
        <p>Payment</p>
      </div>
    </div>
  </div>
</template>
<style scoped lang="scss">
@import "@/assets/css/variables";

.grid-cols-3 {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px;
  margin-bottom: 2rem;
}

.step {
  margin-top: 8px;
  display: flex;
  gap: 12px;
  h4,
  p {
    font-size: 14px;
    line-height: 18px;
    color: rgba(0, 0, 0, 0.45);
    white-space: nowrap;
  }

  span {
    width: 24px;
    height: 24px;
    display: inline-block;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid rgba(0, 0, 0, 0.45);
    color: rgba(0, 0, 0, 0.45);
  }

  .icon {
    margin-top: 16px;
    margin-left: 20px;
    color: rgba(0, 0, 0, 0.45);
    font-size: 20px;
  }
}

.active-step {
  border-bottom: 2px solid $TDC-orange;
  span {
    background: $TDC-orange;
    color: white;
    border: none !important;
  }
  h4,
  p {
    color: black;
  }
}
</style>
