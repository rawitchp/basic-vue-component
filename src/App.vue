<template>
  <div>
    <h4>
      <FormComponent />
    </h4>
    <h4>
      <ListData />
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
};
</script>

<style></style>
