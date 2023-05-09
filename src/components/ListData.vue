<template>
  <ul>
    <Person
      v-for="item in employees"
      :id="item.id"
      :key="item.id"
      :name="item.name"
      :salary="item.salary"
      :department="item.department"
      :isVisible="item.isVisible"
      @show="toggleVisible"
      @delete="deleteEmployee"
    />
  </ul>
</template>

<script>
import Person from './Person.vue';
export default {
  name: 'ListData',
  components: { Person },
  methods: {
    toggleVisible(id) {
      this.employees = this.employees.map((item) => {
        if (item.id === id) {
          return { ...item, isVisible: !item.isVisible };
        }
        return item;
      });
    },
    deleteEmployee(id) {
      this.employees = this.employees.filter((item) => item.id !== id);
    },
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Mix',
          salary: 40000,
          department: 'Programmer',
          isVisible: false,
        },
        {
          id: 2,
          name: 'Max',
          salary: 30000,
          department: 'Accounting',
          isVisible: false,
        },
        { id: 3, name: 'Min', department: 'graphics', isVisible: false },
        {
          id: 4,
          name: 'Milk',
          salary: 15000,
          department: 'Manager',
          isVisible: false,
        },
      ],
    };
  },
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 1rem 0;
}
</style>
