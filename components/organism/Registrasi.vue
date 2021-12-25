<template>
  <div>
    <div
      class="grid gap-8 grid-cols-2 m-20 p-10 rounded-lg items-center bg-green-200"
    >
      <div class="m-10 p-10 bg-white rounded-lg">
        <FormRegistrasi :form-left="formLeft" @onClick="onClick" />
      </div>
      <div class="m-10 p-20 bg-white rounded-lg">
        <DataRegistrasi :data-right="dataRight" />
      </div>
    </div>
  </div>
</template>

<script>
import FormRegistrasi from "~/components/mollecules/FormRegistrasi";
import DataRegistrasi from "~/components/mollecules/DataRegistrasi";
export default {
  components: {
    FormRegistrasi,
    DataRegistrasi,
  },
  props: {
    formLeft: {
      type: Object,
      default: () => ({}),
    },
    dataRight: {
      type: Object,
      default: () => ({}),
    },
  },
  methods: {
    onClick() {
      this.$emit("onClick");
    },
  },
};
</script>

<style></style>
