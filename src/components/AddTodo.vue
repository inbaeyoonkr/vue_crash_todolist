<template>
  <div>
    <form @submit="addTodo">
      <input type="text" v-model="title" name="title" placeholder="Title" />
      <input type="submit" value="Submit" class="btn" />
    </form>
  </div>
</template>

<script>
export default {
  name: 'AddTodo',
  data() {
    return {
      title: '',
    };
  },
  methods: {
    addTodo(e) {
      e.preventDefault();
      const newTodo = {
        title: this.title,
        completed: false,
      };
      // send up to parent
      this.$emit('add-todo', newTodo);
      this.title = '';
    },
  },
};
</script>
<style scoped>
form {
  display: flex;
}
input[type='text'] {
  flex: 1;
}
</style>
