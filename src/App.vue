<template>
  <div id="app">
    <h1>hoidettavia asioita</h1>
    <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todos from "./components/Todos";

export default {
  name: "App",
  components: {
    Todos,
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "Hoida näyttödokumentit",
          completed: false,
        },
        {
          id: 2,
          title: "Tarkista tehtäväpalautukset",
          completed: false,
        },
        {
          id: 3,
          title: "Nauhoita Djangokurssin viimeiset videot",
          completed: false,
        },
        {
          id: 4,
          title: "Tee HOKS testi",
          completed: false,
        },
      ],
    };
  },
  methods: {
    deleteTodo(id) {
      this.todos = this.todos.filter(todo => todo.id !== id);
    },
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
}

body {
  margin-left: 10%;
  max-width: 60%;
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
