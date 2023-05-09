<template>
  <h1>
    <div>{{ message }}</div>
  </h1>
</template>

<script>
export default {
  name: 'Person',
  data() {
    return { message: 'ข้อมูลพนักงาน' };
  },
};
</script>

<style scoped>
h1 {
  color: red;
}
</style>
