<template>
  <div id="app">
   <TodoList></TodoList>
  </div>
</template>

<script>
import TodoList from './components/TodoList/TodoList';

export default {
  name: 'app',
  components: {
    TodoList
  }
}
</script>