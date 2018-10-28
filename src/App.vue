<template>
  <div id="app">
    <todo-input v-on:tasking="createTaskObject">
      <div slot="btn-add-task">
        Special button text
      </div>
    </todo-input>
    <todo-list :tasks="tasks"></todo-list>
  </div>
</template>

<script>
import TodoInput from './components/TodoInput.vue';
import TodoList from './components/TodoList.vue';

export default {
  name: 'app',
  components: {
    TodoInput,
    TodoList
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
  },
  computed: {
    newId() {
      let lastItem = this.tasks[this.tasks.length - 1];
      return lastItem.id + 1;
    }
  },
  methods: {
    createTaskObject: function(name) {
      let taskObj = {
        id: this.newId,
        name,
        status: false
      };
      this.tasks.push(taskObj);
    }
  }
}
</script>

<style lang="scss">

</style>
