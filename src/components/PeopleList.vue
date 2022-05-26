<template>
    <h1>People List</h1>

    <!-- Now with :age it's JS code in quotes
    <PeopleListItem name="Dimon" :age="99" hairColor="grey" />    
    <PeopleListItem name="Dimas" age="89" hairColor="grey" />
    <PeopleListItem name="Dimma" age="42" hairColor="brown" /> -->
    <PeopleListItem :person="person1" />
    <PeopleListItem :person="person2" />
    <PeopleListItem :person="person3" />
</template>

<script>
    import PeopleListItem from './PeopleListItem';
    export default {
        name:   'PeopleList',   
        components: {
            PeopleListItem,            
        },
        data() {
            return {
                person1: {name: 'Dimetrio', age: 42, hairColor: 'brown'},
                person2: {name: 'Dimon', age: 99, hairColor: 'grey'},
                person3: {name: 'Dimas', age: 89, hairColor: 'grey'},
            }
        },
    };    
</script>

<style>
</style>