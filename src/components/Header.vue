<template>
  <header class="header">
    <div>Todo List</div>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>
.header {
  font-size: 2rem;
  font-weight: bold;
  text-align: center;
}
</style>
