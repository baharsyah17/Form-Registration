<template>
  <button class="bg-green-200" @click="$emit('click')">{{ content }}</button>
</template>

<script>
export default {
  props: {
    content: {
      type: String,
      default: "Submit",
    },
  },
};
</script>

<style>
button {
  position: relative;
  border-radius: 15px;
  height: 40px;
  margin-top: 20px;
  padding-left: 60px;
  padding-right: 60px;
  left: 70%;
}
</style>
