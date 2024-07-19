<script setup></script>

<template>
  <div>
    <button v-b-modal.completedSetup>completed Account</button>

    <b-modal
      id="completedSetup"
      hide-header
      hide-footer
      modal-class="custom-modal"
    >
      <b-col cols="12" class="content">
        <div class="icon-container">
          <span>
            <Icon class="icon" icon="lucide:mail-check" />
          </span>
        </div>
        <div class="heading-text">
          <h2>Completed account setup</h2>
          <p>You’ve successfully completed your account setup.</p>
        </div>
        <div class="button">Back to Touchdown Club Homepage</div>
      </b-col>
    </b-modal>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 20px;
}
h2 {
  font-size: 24px;
  line-height: 28px;
  text-align: center;
  font-family: Goldman;
}
p {
  font-size: 14px;
  line-height: 14px;
  text-align: center;
  color: $light-gray;
}

.row {
  display: flex;
  align-items: center;
  gap: 10px;
}

.button {
  border: 1px solid $extra-light;
  margin-top: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px 30px;
  font-size: 14px;
  border-radius: 3px;
}

.icon-container {
  background-color: rgba(51, 255, 0, 0.2);
  height: 80px;
  width: 80px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  .icon {
    color: $TDC-green;
    font-size: 35px;
  }
}
</style>
