<template>
  <ul>
    <todo-item
      v-for="(task, index) in tasks"
      :key="task.id"
      :name="task.name"
      :status="task.status">
    </todo-item>
  </ul>

</template>

<script>
  import TodoItem from './TodoItem.vue';

  export default {
    props: ['tasks'],
    components: {
      TodoItem
    }
  }
</script>

<style>

</style>
