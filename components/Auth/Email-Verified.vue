<script setup></script>

<template>
  <div>
    <b-modal
      id="emailVerified"
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
          <h2>Email verified!</h2>
          <p>
            You’ve successfully verified your email.<br />Final step! Complete
            setting up your account to be <br />
            a member of the club.
          </p>
        </div>

        <button class="button" v-b-modal.verifyEmailPopover type="submit">
          Setup account
        </button>
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

.button {
  all: unset;
  background-color: $TDC-orange;
  border-color: $TDC-orange;
  color: white;
  font-weight: bold;
  padding: 6px 10px;
  width: 100% !important;
  text-align: center;
  border-radius: 3px;
  &:hover {
    background-color: #e05a00;
    border-color: $dark-TDC-orange;
  }
  :focus {
    outline: none;
  }
}

.row {
  display: flex;
  align-items: center;
  gap: 10px;
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

.custom-modal {
  .modal-backdrop {
    backdrop-filter: blur(50px);
    background-color: rgba(0, 0, 0, 0.6);
  }

  .modal-dialog {
    max-width: 560px;
  }
  .modal-content {
    padding: 40px;
  }
}
</style>
