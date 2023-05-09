<template>
  <li>
    <img
      src="https://creazilla-store.fra1.digitaloceanspaces.com/icons/7911322/avatar-icon-sm.png"
    />
    <hr />
    <slot name="card-header"></slot>
    <slot name="card-button"></slot>
    <slot name="card-content"></slot>
  </li>
</template>

<script>
export default { name: 'Card' };
</script>

<style scoped>
li {
  margin: 1rem 0;
  font-size: 1.25rem;
  font-weight: bold;
  background: skyblue;
  padding: 0.5rem;
  color: #1f1f1f;
  border-radius: 25px;
}
img {
  width: 100px;
  height: 100px;
}
</style>
