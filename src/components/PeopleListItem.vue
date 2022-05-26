<template>
  <div>
    <!-- After changing props these are different
        <h3>{{ name }}</h3>
        <p>Age: {{ age }} years</p>
        <p>Hair Color: {{ hairColor }}</p> -->

    <!-- Now these are prefixed with props name -->
    <h3>{{ person.name }}</h3>
    <p>Age: {{ person.age }} years</p>
    <p>Hair Color: {{ person.hairColor }}</p>
  </div>
</template>

<script>
export default {
  name: "PeopleListItem",
  // props:  ['name', 'age', 'hairColor'], // Changed to the object below:
  props: ["person"],
};
</script>

<style></style>
