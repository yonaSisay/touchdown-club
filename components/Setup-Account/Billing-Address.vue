<script setup>
import { ref } from "vue";

const selected = ref(null);
const region = ref([
  { value: null, text: "Please select an option" },
  { value: "a", text: "United States" },
  { value: "b", text: "Canada" },
  { value: { C: "3PO" }, text: "England" },
]);
const states = ref([
  { value: null, text: "select state" },
  { value: "a", text: "New York" },
  { value: "b", text: "Washington DC" },
  { value: { C: "3PO" }, text: "California" },
]);
</script>

<template>
  <div>
    <h3 class="title">Billing address</h3>
    <p class="sub-title">
      Select the address that matches your card or payment method.
    </p>
    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>Country/Region</label
        >
        <b-form-select v-model="selected" :options="region"></b-form-select>
      </b-col>
    </b-row>
    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>First Name</label
        >
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="E.g. John"
          class="custom-input"
        ></b-form-input
      ></b-col>
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>Last name</label
        >
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="E.g. Doe"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>

    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none">Company name</label>
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="E.g. XYX Company"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>
    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none">Address</label>
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="United States"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>

    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>City</label
        >
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="Enter City"
          class="custom-input"
        ></b-form-input
      ></b-col>
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>State</label
        >
        <b-form-select v-model="selected" :options="states"></b-form-select>
      </b-col>
      <b-col>
        <label class="label" for="input-none"
          ><span class="star">*</span>Zip Code</label
        >
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="E.g. Doe"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>

    <b-row class="mt-3">
      <b-col>
        <label class="label" for="input-none">Phone</label>
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="Enter Phone Number"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>
  </div>
</template>
<style scoped lang="scss">
@import "@/assets/css/variables";

.title {
  font-size: 18px;
  font-weight: 600;
}

.sub-title {
  font-size: 14px;
  color: gray;
}

.label {
  font-weight: 400;
  font-size: 1rem;
  display: flex;
  align-items: center;
  gap: 5px;
}
</style>
