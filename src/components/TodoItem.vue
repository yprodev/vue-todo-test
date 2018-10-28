<template>
  <li v-if="status">{{ name }}</li>
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


</style>
