<template>
  <div>
    <h1>People List</h1>
    <PeopleListItem
      v-for="person in people"
      :key="person.name"
      :person="person"
    />
  </div>
</template>

<script>
import PeopleListItem from "./PeopleListItem.vue";

export default {
  name: "PeopleList",
  components: {
    PeopleListItem,
  },
  data() {
    return {
      people: [
        { name: "Dimetrio", age: 42, hairColor: "brown" },
        { name: "Dimon", age: 99, hairColor: "grey" },
        { name: "Dimas", age: 89, hairColor: "grey" },
      ],
    };
  },
};
</script>

<style scoped>
h1 {
  color: brown;
}
</style>

<!-- Now with :age it's JS code in quotes
    <PeopleListItem name="Dimon" :age="99" hairColor="grey" />
    <PeopleListItem name="Dimas" age="89" hairColor="grey" />
    <PeopleListItem name="Dimma" age="42" hairColor="brown" />
    <PeopleListItem :person="person1" />
    <PeopleListItem :person="person2" />
    <PeopleListItem :person="person3" /> -->
