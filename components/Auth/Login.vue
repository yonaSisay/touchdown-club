<script setup></script>

<template>
  <div>
    <b-button
      v-b-modal.loginPopover
      variant="outline-light"
      class="custom-button"
      >Login</b-button
    >

    <b-modal
      id="loginPopover"
      hide-header
      hide-footer
      modal-class="custom-modal"
    >
      <h2>Hey!<span></span></h2>
      <p class="sub-title-p">Welcome back! Please enter your details.</p>

      <b-col class="custom-col">
        <b-row>
          <label for="input-none">Email</label>
          <b-form-input
            id="input-none"
            :state="null"
            placeholder="E.g. johndoe@mail.com"
            class="custom-input"
          ></b-form-input>
        </b-row>
        <b-row class="mt-4">
          <label for="input-none">Password</label>
          <b-form-input
            id="input-none"
            :state="null"
            placeholder="********"
            type="password"
          ></b-form-input>
        </b-row>
        <div class="mt-4 recap-sign">
          <img src="@/assets/temp/reCAPTCHA v2 checkbox.png" alt="recaptcha" />
        </div>
        <b-row class="checkbox mt-4">
          <b-form-checkbox
            id="checkbox-1"
            name="checkbox-1"
            value="accepted"
            unchecked-value="not_accepted"
          >
            Remember me
          </b-form-checkbox>
          <p>Forgot password?</p>
        </b-row>
        <div class="mt-4 recap-sign">
          <button type="submit">Log in</button>
        </div>
      </b-col>
      <b-row class="break-line mt-4">
        <span />
        OR
        <span />
      </b-row>
      <b-col class="mt-4 third-party">
        <div>
          <Icon class="facebook" icon="jam:facebook" /> Log in via Facebook
        </div>
        <div>
          <Icon class="google" icon="devicon:google" /> Log in via Google
        </div>
      </b-col>
      <b-row class="mt-4 sign-in">
        Don’t have an account?? <span>Sign up for free</span>
      </b-row>
    </b-modal>
  </div>
</template>

<style scoped lang="scss">
@import "@/assets/css/variables";

h2 {
  font-family: Goldman;
  font-size: 24px;
  line-height: 28px;
  display: flex;
  align-items: center;
  gap: 5px;

  span {
    background: $TDC-orange;
    width: 1.2rem;
    height: 1.2rem;
    display: inline-block;
    border-radius: 50%;
  }
}
.third-party {
  div {
    border: 1px solid $extra-light;
    margin-top: 8px;
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 10px;
    border-radius: 3px;
    gap: 10px;
    .facebook {
      font-size: 30px;
      color: blue;
    }
    .google {
      font-size: 25px;
    }
  }
}

.sign-in {
  display: flex;
  justify-content: center;
  gap: 10px;
  span {
    color: $TDC-orange;
    font-weight: 500;
  }
}

.custom-input {
  border: 1px solid $extra-light;
}

.break-line {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  color: $extra-light;
  span {
    height: 0.5px;
    border: 0.2px solid $extra-light;
    display: inline-block;
    text-align: center;
    padding: 0 10px;
    width: 40%;
  }
}

.custom-col {
  label {
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
  }
}

.recap-sign {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 0 3rem;
  img {
    width: 423px !important;
    object-fit: fill;
  }
  button {
    all: unset;
    background-color: $TDC-orange;
    border-color: $TDC-orange;
    color: white;
    font-weight: bold;
    padding: 12px 30px;
    width: 100% !important;
    text-align: center;
    border-radius: 3px;
    &:hover {
      background-color: #e05a00;
      border-color: $dark-TDC-orange;
    }
    &:focus {
      outline: none;
    }
  }
}

.checkbox {
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  display: flex;
  justify-content: space-between;
  p {
    color: $water-blue;
    font-weight: 700;
  }
}

.sub-title-p {
  font-family: Inter;
  font-size: 14px;
  line-height: 21px;
  font-weight: 400;
  color: $light-gray;
}

.custom-modal {
  .modal-backdrop {
    backdrop-filter: blur(50px);
    background-color: rgba(0, 0, 0, 0.6);
  }

  .modal-dialog {
    max-width: 600px;
  }
  .modal-content {
    padding: 40px;
  }
}
</style>
