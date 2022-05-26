<template>
  <div>
    <h1 v-if="shouldShowMessage">{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: "FlashingMessage",
  props: ["message", "delay"],
  data() {
    return {
      shouldShowMessage: true,
    };
  },
  created() {
    setInterval(() => {
      this.shouldShowMessage = !this.shouldShowMessage;
    }, this.delay);
  },
};
</script>

<style></style>
