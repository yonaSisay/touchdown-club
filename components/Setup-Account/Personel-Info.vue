<template>
  <div>
    <b-row>
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

    <b-row class="mt-4">
      <b-col>
        <label class="label" for="input-none">Company name</label>
        <b-form-input
          id="input-none"
          :state="null"
          placeholder="E.g. ABC Company"
          class="custom-input"
        ></b-form-input
      ></b-col>
    </b-row>
  </div>
</template>
<style scoped lang="scss">
@import "@/assets/css/variables";

.label {
  font-weight: 400;
  font-size: 1rem;
  display: flex;
  align-items: center;
  gap: 5px;
}
</style>
