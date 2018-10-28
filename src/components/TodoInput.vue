<template>
  <div>
    <input type="text"
           placeholder="Type your task.."
           v-model="newValue"
           @keyup.enter="addTask">
    <button @click="addTask"
            :disabled="newValue === ''">
      <slot name="btn-add-task">Add Todo</slot>
    </button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        newValue: ''
      };
    },
    methods: {
      addTask() {
        this.$emit('tasking', this.newValue);
        this.newValue = '';
      },
      isValue() {
        return this.newValue !== '';
      }
    },
    mounted() {

    }
  }

</script>

<style>


</style>
