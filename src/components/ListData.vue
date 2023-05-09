<template>
  <Person name="Mix" salary="20000" />
  <Person name="Max" salary="22000" />
  <Person name="Min" salary="15000" />
  <Person name="Milk" salary="14000" />
</template>

<script>
import Person from './Person.vue';
export default {
  name: 'ListData',
  components: { Person },
};
</script>

<style></style>
