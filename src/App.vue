<template>
  <div id="app">
    <center>
      <h1>hoidettavia asioita</h1>
      <Todos v-bind:todos="todos" />
    </center>
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
      ],
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
