<template>
  <li :class="{ 'completed': status }">{{ name }}</li>
</template>

<script>
  export default {
    props: {
      status: { required: true },
      name: { required: true },
    }
  }
</script>

<style>
  .completed {
    text-decoration: line-through;
  }
</style>
