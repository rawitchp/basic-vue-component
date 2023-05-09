<template>
  <h1>
    <div>Name: {{ name }} Salary: {{ salary }}</div>
  </h1>
</template>

<script>
export default {
  name: 'Person',
  props: {
    name: { type: String, required: true },
    salary: {
      type: Number,
      default: 12000,
    },
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
