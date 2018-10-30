<template>
  <ul>
    <common-item
      v-for="task in tasks"
      :key="task.id"
      :task="task">
    </common-item>
  </ul>
</template>

<script>
  import CommonItem from '../common/CommonItem.vue';

  export default {
    components: {
      CommonItem
    },
    props: {
      tasks: {
        type: Array
      }
    }
  }
</script>
