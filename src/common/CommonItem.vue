<template>
  <li :class="{ 'completed': task.status }">
    {{ task.name }}
    <button @click="onToggle" class="btnToggle">
      x
    </button>
  </li>
</template>

<script>
  export default {
    name: 'CommonItem',
    props: {
      task: {
        type: Object,
        required: true
      }
    },
    methods: {
      onToggle() {
        return this.task.status = !this.task.status
      }
    }
  }
</script>

<style>
  .completed {
    text-decoration: line-through;
  }

  .btnToggle {
    display: inline-block;
    padding: 2px 5px;
    margin: 0 15px;
    background: #c3c3c3;
    border: 0;
    color: white;
    outline: none;
  }
</style>
