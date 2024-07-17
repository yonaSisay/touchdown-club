<script setup></script>

<template>
  <div>
    <b-modal
      id="verifyEmailPopover"
      hide-header
      hide-footer
      modal-class="custom-modal"
    >
      <b-col cols="12" class="content">
        <div class="icon-container">
          <span>
            <Icon class="icon" icon="bi:send" />
          </span>
        </div>
        <div class="heading-text">
          <h2>Check your email</h2>
          <p>We sent a verification link to</p>
          <span>johndoe@gmail.com</span>
        </div>
        <b-row class="row"
          >Didn’t receive the email? <span>Click to resend</span></b-row
        >
        <div class="button">Back to Touchdown Club Homepage</div>
      </b-col>
    </b-modal>
  </div>
</template>

<style lang="scss">
@import "@/assets/css/variables";
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 20px;
  h2 {
    font-size: 24px;
    line-height: 28px;
    text-align: center;
  }
  p {
    font-size: 14px;
    line-height: 14px;
    text-align: center;
    color: $light-gray;
  }
  span {
    display: block;
    font-size: 14px;
    text-align: center;
    color: $TDC-orange;
    font-weight: 600;
    line-height: 5px;
  }
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

.row {
  display: flex;
  align-items: center;
  gap: 10px;
}

.icon-container {
  background-color: rgba(255, 165, 0, 0.2);
  height: 80px;
  width: 80px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  .icon {
    color: $TDC-orange;
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
