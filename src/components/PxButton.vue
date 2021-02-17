<template>
  <button
    @click="buttonClick"
    class="bg-transparent hover:bg-green text-green font-semibold hover:text-white py-2 px-2 border border-green hover:border-transparent rounded"
  >
    <beat-loader :loading="isLoading" :color="'#68d391'" :size="8" />
    <p v-show="!isLoading">
      <slot></slot>
    </p>
  </button>
</template>

<script>
export default {
  name: "PxButton",

  props: {
    isLoading: {
      type: Boolean,
      default: false
    }
  },

  methods: {
    buttonClick() {
      this.$emit("click");
    }
  }
};
</script>
