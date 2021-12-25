<template>
  <div>
    <h1 class="text-2xl font-bold text-center">Registration Form</h1>
    <br />
    <TextInput label="First Name" v-model="formLeft.firstName" />
    <TextInput label="Last Name" v-model="formLeft.lastName" />
    <Radio
      v-model="formLeft.gender"
      name="gender"
      input-value="Man"
      label="Man"
    />
    <Radio
      v-model="formLeft.gender"
      name="gender"
      input-value="Woman"
      label="Woman"
    />
    <TextInput label="Email" v-model="formLeft.email" />
    <TextInput label="Phone Number" v-model="formLeft.phoneNumber" />
    <TextInput label="Address" v-model="formLeft.address" />
    <TextInput label="Postal Code" v-model="formLeft.postalCode" />
    <Submit @click="submitData" />
  </div>
</template>

<script>
import TextInput from "~/components/atoms/TextInput.vue";
import Radio from "~/components/atoms/RadioInput.vue";
import Submit from "../atoms/Submit.vue";
export default {
  components: { TextInput, Radio, Submit },
  props: {
    formLeft: {
      type: Object,
      default: () => ({}),
    },
  },
  data() {
    return {
      tes: "",
    };
  },
  methods: {
    submitData() {
      this.$emit("onClick");
    },
  },
};
</script>

<style></style>
