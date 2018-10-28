<template>
  <div>
    <input type="text"
           placeholder="Type your task.."
           v-model="newValue">
    <button @click="$emit('adding-new-task', newValue)">Add Todo</button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        newValue: ''
      };
    },
  }

</script>

<style>


</style>
