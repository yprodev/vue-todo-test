<template>
  <div id="app">
    <todo-input></todo-input>
  </div>
</template>

<script>
import TodoInput from './components/TodoInput.vue';

export default {
  name: 'app',
  components: {
    TodoInput
  },
  data () {
    return {
      tasks: [
        { id: 1, name: 'Go to the park', done: true },
        { id: 2, name: 'Make imposible', done: false },
        { id: 3, name: 'Make additional bonus', done: true },
        { id: 4, name: 'Make homework', done: false },
        { id: 5, name: 'Go to bed', done: false },
      ]
    };
  }
}
</script>

<style lang="scss">

</style>
