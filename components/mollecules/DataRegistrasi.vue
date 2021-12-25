<template>
  <div>
    <h1 class="text-2xl font-bold text-center">Registration Data</h1>
    <br />
    <TextInput
      label="First Name"
      v-model="dataRight.firstName"
      :input-value="dataRight.firstName"
    />
    <TextInput
      label="Last Name"
      v-model="dataRight.lastName"
      :input-value="dataRight.lastName"
    />
    <TextInput
      label="Gender"
      v-model="dataRight.gender"
      :input-value="dataRight.gender"
    />
    <TextInput
      label="Email"
      v-model="dataRight.email"
      :input-value="dataRight.email"
    />
    <TextInput
      label="Phone Number"
      v-model="dataRight.phoneNumber"
      :input-value="dataRight.phoneNumber"
    />
    <TextInput
      label="Address"
      v-model="dataRight.address"
      :input-value="dataRight.address"
    />
    <TextInput
      label="Postal Code"
      v-model="dataRight.postalCode"
      :input-value="dataRight.postalCode"
    />
  </div>
</template>

<script>
import TextInput from "~/components/atoms/TextInput.vue";
import RadioInput from "~/components/atoms/RadioInput.vue";
export default {
  components: { TextInput, RadioInput },
  props: {
    dataRight: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style></style>
