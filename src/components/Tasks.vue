<template>
  <ul>
    <li :class="{'completed':task.completed}" v-for="task in tasks" @click="task.completed = ! task.completed">{{ task.name }}</li>
  </ul>
</template>

<script>
  export default {
    data () {
      return {
        tasks: [
          { name: 'Check budget', completed: false },
          { name: 'Pick up milk', completed: false },
          { name: 'Write some code', completed: true }
        ]
      }
    }
  }
</script>
<style>
    .completed {
        text-decoration: line-through;
    }
</style>