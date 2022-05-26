<template>
  <div>
    <p>You have clicked the button {{ numberOfClicks }} times</p>
    <!--
        <button @click="increment">Click Me</button>
        <button @click="reset">Reset</button> -->
    <!-- Passing this to the parent component -->
    <button @click="$emit('increment')">Click Me</button>
    <button @click="$emit('reset')">Reset</button>
  </div>
</template>

<script>
export default {
  name: "CounterButton",
  props: ["numberOfClicks"],
  emits: ["increment", "reset"],
};
</script>

<style>
button {
  margin: 5px;
}
</style>
