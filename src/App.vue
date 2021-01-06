<template>
  <div id="app">
    <Todos
      v-bind:todos="todos"
      v-on:del-todo="deleteTodo"
      v-on:change-complete="changeCompleted"
    />
  </div>
</template>

<script>
import Todos from "./components/Todos.vue";
export default {
  name: "app",
  components: {
    Todos,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Todo One",
          completed: false,
        },
        {
          id: 2,
          title: "Todo Two",
          completed: true,
        },
        {
          id: 3,
          title: "Todo Three",
          completed: false,
        },
      ],
    };
  },
  methods: {
    changeCompleted(id) {
      let index = this.todos.findIndex((x) => x.id === id);
      this.todos[index].completed = !this.todos[index].completed;
    },
    deleteTodo(id) {
      this.todos = this.todos.filter((todo) => todo.id !== id);
    },
  },
};
</script>

<style></style>
