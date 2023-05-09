<template>
  <div>
    <h4>
      <FormComponent />
    </h4>
    <h4>
      <ListData :employees="employees" />
    </h4>
  </div>
</template>

<script>
import FormComponent from './components/FormComponent.vue';
import ListData from './components/ListData.vue';

export default {
  name: 'App',
  components: {
    ListData,
    FormComponent,
  },
  data() {
    return {
      employees: [
        { name: 'Mix', salary: 40000 },
        { name: 'Max', salary: 30000 },
        { name: 'Min' },
        { name: 'Milk', salary: 15000 },
      ],
    };
  },
};
</script>

<style></style>
