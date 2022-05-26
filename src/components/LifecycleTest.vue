<template>
  <div>
    <h1>This is a lifecycle test</h1>
  </div>
</template>

<script>
export default {
  name: "LifecycleTest",
  props: ["numberOfClicks"],
  beforeCreate() {
    console.log("In beforeCreate");
  },
  created() {
    console.log("In created");
  },
  beforeMount() {
    console.log("In beforeMount");
  },
  mounted() {
    console.log("In mounted");
  },
  beforeUpdate() {
    console.log("In beforeUpdate");
  },
  updated() {
    console.log("Updated");
  },
  beforeUnmount() {
    console.log("In beforeUnmounted");
  },
  unmounted() {
    console.log("Now unmounted");
  },
};
</script>

<style></style>
