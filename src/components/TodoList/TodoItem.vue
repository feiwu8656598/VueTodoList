<template>
  <li>
    {{value}}
    <edit-todo-item-area v-show="showEditArea"/>
    <button @click="deleteTodoItem">delete</button>
  </li>
</template>

<script>
import EditTodoItemArea from "./EditTodoItemArea";

export default {
  name: "TodoItem",
  components: {
    EditTodoItemArea
  },
  data() {
    return {
      showEditArea: false
    };
  },
  props: {
    id: Number,
    value: String
  },
  methods: {
    deleteTodoItem: function() {
      this.$emit("deleteTodoItem", this.id);
    }
  }
};
</script>

