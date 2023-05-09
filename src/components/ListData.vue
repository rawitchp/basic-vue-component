<template>
  <ul>
    <Person
      v-for="(item, i) in employees"
      :key="i"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :gender="item.gender"
      :skill="item.skill"
    />
  </ul>
</template>

<script>
import Person from './Person.vue';
import Card from './Card.vue';
export default {
  name: 'ListData',
  components: {
    Person,
    Card,
  },
  props: ['employees'],
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 1rem 0;
}
</style>
