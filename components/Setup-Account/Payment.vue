<script setup>
import { computed, ref, watch } from "vue";

const emits = defineEmits(["paymentType"]);
const selected = ref("card");

watch(
  selected,
  () => {
    emits("paymentType", selected.value);
  },
  { immediate: true }
);
</script>

<template>
  <div>
    <h3 class="">Payment</h3>
    <p>All transactions are secure and encrypted.</p>
    <div class="accordion mb-4" role="tablist">
      <b-card no-body>
        <b-card-header
          header-tag="header"
          class="p-3"
          :class="{ 'accordion-header': selected != 'paypal' }"
          role="tab"
        >
          <div
            class="flex-between"
            block
            @click="selected = 'card'"
            v-b-toggle.accordion-1
          >
            <b-form-radio
              v-model="selected"
              :aria-describedby="ariaDescribedby"
              disabled
              class="text-black"
              name="some-radios"
              value="card"
              >Credit Card</b-form-radio
            >
            <img src="~/assets/payments.png" alt="payments" />
          </div>
        </b-card-header>
        <b-collapse
          id="accordion-1"
          visible
          accordion="my-accordion"
          role="tabpanel"
          class="credit-body"
        >
          <b-card-body>
            <b-row class="mt-3">
              <b-col>
                <b-form-input
                  id="input-none"
                  :state="null"
                  placeholder="Card Number"
                  class="custom-input text-light-gray"
                ></b-form-input
              ></b-col>
            </b-row>

            <b-row class="mt-3">
              <b-col>
                <b-form-input
                  id="input-none"
                  :state="null"
                  placeholder="Name on Card"
                  class="custom-input"
                ></b-form-input
              ></b-col>
            </b-row>
            <b-row class="mt-3">
              <b-col>
                <b-form-input
                  id="input-none"
                  :state="null"
                  placeholder="Expiration date (MM / YY)"
                  class="custom-input"
                ></b-form-input
              ></b-col>
              <b-col>
                <b-input-group>
                  <b-form-input
                    id="input-none"
                    :state="null"
                    placeholder="Security code"
                    class="custom-input"
                  ></b-form-input>

                  <b-input-group-append is-text>
                    <Icon
                      icon="iconoir:question-mark-circle"
                      width="22px"
                      v-b-tooltip.hover
                      title="3-digit security code usually found on the back of your card. American Express cards have 4-digit code located on the front."
                    />
                  </b-input-group-append>
                </b-input-group>
              </b-col>
            </b-row>
          </b-card-body>
        </b-collapse>
      </b-card>

      <b-card no-body class="mb-1">
        <b-card-header
          header-tag="header"
          class="p-3"
          :class="{ 'accordion-header': selected != 'card' }"
          role="tab"
        >
          <div
            class="flex-between"
            block
            @click="selected = 'paypal'"
            v-b-toggle.accordion-2
          >
            <b-form-radio
              v-model="selected"
              :aria-describedby="ariaDescribedby"
              name="some-radios"
              value="paypal"
              disabled
              >Pay Pal</b-form-radio
            >
            <img src="~/assets/paypal.png" alt="payments" />
          </div>
        </b-card-header>
        <b-collapse id="accordion-2" accordion="my-accordion" role="tabpanel">
          <b-card-body>
            <b-card-text class="text-center"
              >After clicking "Pay with PayPal", you will be redirected to
              PayPal to complete your purchase securely.
            </b-card-text>
          </b-card-body>
        </b-collapse>
      </b-card>
    </div>

    <SetupAccountBillingAddress v-if="selected == 'card'" />
  </div>
</template>
<style scoped lang="scss">
@import "@/assets/css/variables";

.accordion-header {
  border: 1px solid $TDC-orange;
  border-radius: 10px;
  background: $light-TDC-orange !important;
  cursor: pointer;
}

.credit-body {
  background: rgba(218, 218, 218, 1);
}

.text-light-gray {
  ::placeholder {
    color: rgba(0, 0, 0, 0.25) !important;
  }
}

div {
  h3 {
    font-size: 18px;
    font-weight: 600;
  }

  p {
    font-size: 14px;
    color: gray;
  }
}
</style>
