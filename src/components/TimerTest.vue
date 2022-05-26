<template>
  <div>
    <h1>I'm the timer</h1>
  </div>
</template>

<script>
export default {
  name: "TimerTest",
  props: ["delay", "name"],
  emits: ["tick"],
  created() {
    setInterval(() => {
      this.$emit("tick", this.name);
    }, this.delay);
  },
};
</script>

<style></style>
