<template>
  <div>
    <div v-bind:key="todo.id" v-for="todo in todos">
      <todoitem />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
import Todoitem from "./Todoitem.vue";

export default {
  name: "Todos",
  components: {
    Todoitem,
  },
  props: ["todos"],
};
</script>

<style scoped>
</style>