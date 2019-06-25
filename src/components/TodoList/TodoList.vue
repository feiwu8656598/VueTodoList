<template>
  <div>
    <ul>
      <todo-item
        v-for="item of lists"
        :key="item.id"
        :id="item.id"
        :value="item.value"
        @deleteTodoItem="deleteTodoItem"
      ></todo-item>
    </ul>
    <add-todo-item @addTodoItem="addTodoItem"/>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
import AddTodoItem from "./AddTodoItem";

export default {
  name: "TodoList",
  components: {
    TodoItem,
    AddTodoItem
  },
  data() {
    return {
      count: 0,
      lists: []
    };
  },
  methods: {
    addTodoItem: function(value) {
      alert(this.count);
      this.lists.push({
        id: this.count++,
        value: value
      });
    },
    deleteTodoItem: function(id) {
      this.lists.splice(this.lists.findIndex(_ => _.id === id), 1);
    }
  }
};
</script>

