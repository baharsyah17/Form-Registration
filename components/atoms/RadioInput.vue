<template>
  <div>
    <label class="ml-5" :for="label">
      <input
        type="radio"
        :name="name"
        :id="label"
        :value="inputValue"
        @change="onChange"
      />
      {{ label }}
    </label>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: "",
    },
    label: {
      type: String,
      default: "",
    },
    inputValue: {
      type: String,
      default: "",
    },
  },
  methods: {
    onChange(e) {
      this.$emit("input", this.inputValue);
    },
  },
};
</script>

<style></style>
