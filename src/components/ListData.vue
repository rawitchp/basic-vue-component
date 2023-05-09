<template>
  <h1>
    <div>{{ message }}</div>
  </h1>
  <Person />
  <Person />
</template>

<script>
import Person from './Person.vue';
export default {
  name: 'ListData',
  components: { Person },
  data() {
    return {
      message: 'แสดงรายชื่อพนักงานทุกคน',
    };
  },
};
</script>

<style></style>
