<template>
  <div>
    <edit-todo-item-area place-holder="Add a new todo item" ref="baseItem"/>
    <button @click="addTodoItem">Add</button>
  </div>
</template>

<script>
import EditTodoItemArea from "./EditTodoItemArea";
export default {
  components: {
    EditTodoItemArea
  },
  methods: {
    addTodoItem: function() {
      this.$emit("addTodoItem", this.$refs.baseItem.$el.value);
    }
  }
};
</script>
