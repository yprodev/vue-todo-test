<template>
  <div>
    <input type="text"
      placeholder="Type your task.."
      v-model="inputValue"
      @keyup.enter="addTask">
    <button @click="addTask"
      :disabled="isDisabled()">
      <slot name="btn-add-task">
        Add Todo
      </slot>
    </button>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        inputValue: ''
      };
    },
    methods: {
      addTask() {
        if (this.isDisabled()) return;
        this.$emit('tasking', this.inputValue);
      },
      isDisabled() {
        return this.inputValue === '';
      }
    }
  }
</script>
