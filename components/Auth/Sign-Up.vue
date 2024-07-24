<script setup></script>

<template>
  <div>
    <button v-b-modal.signUpPopover class="orange-button" type="submit">
      Register now
      <Icon icon="lucide:chevrons-right" />
    </button>
    <b-modal
      id="signUpPopover"
      hide-header
      hide-footer
      modal-class="custom-modal"
    >
      <h2>Create an account<span></span></h2>
      <p class="sub-title-p">
        Let’s get started with your Touchdown Club account.
      </p>

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
        <b-row class="mt-4">
          <b-form-checkbox
            id="checkbox-1"
            name="checkbox-1"
            value="accepted"
            unchecked-value="not_accepted"
            class="checkbox"
          >
            I’ve read and accepted <span>Terms of Service</span> and
            <span>Privacy Policy </span>
          </b-form-checkbox></b-row
        >
        <recaptcha id="v2-normal" />
        <div class="mt-4 recap-sign">
          <img src="@/assets/temp/reCAPTCHA v2 checkbox.png" alt="recaptcha" />
          <button v-b-modal.verifyEmailPopover type="submit">Sign up</button>
        </div>
      </b-col>
      <b-row class="break-line mt-4">
        <span />
        OR
        <span />
      </b-row>
      <b-col class="mt-4 third-party">
        <div>
          <Icon class="facebook" icon="jam:facebook" /> Sign up via Facebook
        </div>
        <div>
          <Icon class="google" icon="devicon:google" /> Sign up via Google
        </div>
      </b-col>
      <b-row class="mt-4 sign-in">
        Already have an account? <span>Login here</span>
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
    display: block;
    margin-top: 1rem;
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
