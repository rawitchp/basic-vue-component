<template>
  <Card>
    <template v-slot:card-header>
      <h1>Name: {{ name }}</h1>
    </template>

    <template v-slot:card-content>
      <div>Salary: {{ salary }}</div>
      <div>Department: {{ department }}</div>
      <div>Gender: {{ gender }}</div>
      <ul>
        <li v-for="(item, i) in skill" :key="i">{{ item }}</li>
      </ul>
    </template>
  </Card>
</template>

<script>
import Card from './Card.vue';
export default {
  name: 'Person',
  props: {
    id: {
      type: Number,
    },
    name: { type: String, required: true },
    salary: {
      type: Number,
      default: 12000,
    },
    department: { type: String, required: true },
    gender: {
      type: String,
    },
    skill: { type: Array },
  },
  components: { Card },
};
</script>

<style scoped>
button {
  font: inherit;
  cursor: poniter;
  border: 1px solid #ff0077;
  background: #ff0077;
  color: white;
  padding: 0.05rem 1rem;
  box-shadow: 1px 1px 2px rgba(0, 0, 0, 0);
  border-radius: 5px;
  margin-bottom: 10px;
}
.fade-enter-from {
  opacity: 0;
}
.fade-enter-active {
  transition: all 0.5s linear;
}
</style>
