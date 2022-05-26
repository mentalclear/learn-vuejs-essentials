<template>
  <div>
    <h1 v-if="numberOfClicks > 9">
      Congratulations! You've reached {{ numberOfClicks }} clicks!
    </h1>
    <p v-if="numberOfClicks > 9">Today is: {{ currentDate }}</p>
  </div>
</template>

<script>
export default {
  name: "CongratulationsMsg",
  props: ["numberOfClicks", "currentDate"],
};
</script>

<style></style>
