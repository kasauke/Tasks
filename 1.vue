<template>
  <div class="task-item">
    <h3>{{ task.title }}</h3>
    <p>{{ task.text }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  task: { id: string; title: string; text: string };
}>();
</script>

<style scoped>
.task-item {
  padding: 16px;
  border: 1px solid #ccc;
  border-radius: 6px;
  background: #f9f9f9;
  margin-bottom: 12px;
  text-align: left;
  font-family: sans-serif;
}

h3 {
  margin: 0 0 8px;
  font-size: 1.1em;
  color: #333;
}

p {
  margin: 0;
  color: #666;
  line-height: 1.4;
}
</style>
