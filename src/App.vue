<template>
  <div id="app">
    <todo-input></todo-input>
    <todo-list>
      <todo-item
        v-for="(task, index) in tasks"
        :key="task.id"
        :name="task.name"
        :status="task.status">
      </todo-item>
    </todo-list>
  </div>
</template>

<script>
import TodoInput from './components/TodoInput.vue';
import TodoList from './components/TodoList.vue';
import TodoItem from './components/TodoItem.vue';

export default {
  name: 'app',
  components: {
    TodoInput,
    TodoList,
    TodoItem
  },
  data () {
    return {
      tasks: [
        { id: 1, name: 'Go to the park', status: true },
        { id: 2, name: 'Make imposible', status: false },
        { id: 3, name: 'Make additional bonus', status: true },
        { id: 4, name: 'Make homework', status: false },
        { id: 5, name: 'Go to bed', status: false },
      ]
    };
  }
}
</script>

<style lang="scss">

</style>
