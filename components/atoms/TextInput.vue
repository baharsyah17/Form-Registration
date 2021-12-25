<template>
  <label class="ml-5" :for="label">
    {{ label }}
    <br />
    <input
      type="text"
      class="border-4 border-indigo-500/75"
      :value="inputValue"
      @input="inputData"
    />
  </label>
</template>

<script>
export default {
  props: {
    inputValue: {
      type: String | Number,
      default: "",
    },
    label: {
      type: String,
      default: "",
    },
    pHolder: {
      type: String,
      default: "",
    },
  },
  methods: {
    inputData(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>

<style>
input {
  margin-left: 10px;
  margin-top: 10px;
  margin-bottom: 10px;
  border-radius: 10px;
  padding-right: 75%;
}
</style>
