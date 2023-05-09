<template>
  <Card>
    <template v-slot:card-header>
      <h1>Name: {{ name }}</h1>
    </template>
    <template v-slot:card-button>
      <button @click="showDescription(id)">ดูรายละเอียด</button>&nbsp;
      <button @click="deleteEmployee(id)">ลบข้อมูล</button>
    </template>
    <template v-slot:card-content>
      <transition name="fade">
        <div v-show="isVisible">
          Salary: {{ salary }} Department: {{ department }}
        </div>
      </transition>
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
    isVisible: { type: Boolean, required: true },
  },
  components: { Card },
  methods: {
    showDescription(id) {
      this.$emit('show', id);
    },
    deleteEmployee(id) {
      this.$emit('delete', id);
    },
  },
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
