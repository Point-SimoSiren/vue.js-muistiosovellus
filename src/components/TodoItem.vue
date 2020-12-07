<template>
  <div>
    <p>Todo Item</p>
  </div>
</template>

<script>
export default {
  name: "Todo",
};
</script>

<style scoped>
.todo-item {
  background-color: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}

.is-complete {
  text-decoration: line-through;
}

.del {
  background: red;
  color: #fff;
  border: none;
  padding: 5px, 9px;
  border-radius: 50%;
  cursor: pointer;
  float: right;
}
</style>