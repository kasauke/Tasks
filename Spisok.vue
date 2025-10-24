<template>
  <div>
    <h1>Список дел</h1>
    <p>Всего дел: {{ tasks.length }}</p>
    <div class="tasks">
      <TaskItem
        v-for="task in tasks"
        :key="task.id"
        :task="task"
      />
    </div>
  </div>
  
</template>

<script setup lang="ts">
import { ref } from "vue";
import TaskItem from "./components/TaskItem.vue";

const tasks = ref([
  { 
    id: "1", 
    title: "Пройти утреннюю зарядку", 
    text: "15 минут растяжки и физических упражнений" 
  },
  { 
    id: "2", 
    title: "Выполнить домашнюю работу", 
    text: "Посмотреть задание, Прочитать лекцию, Сделать задание, отправить отчёт" 
  },
  { 
    id: "3", 
    title: "Прогулка", 
    text: "ВЫйти на улицу, погулять пару часов" 
  },
  { 
    id: "4", 
    title: "Поиграть в игры", 
    text: "Позвать друзей и поиграть" 
  } 
]);
</script>

<style>
.tasks {
  display: flex;
  gap: 16px;
  flex-direction: column;
  max-width: 600px;
  margin: 0 auto;
}

h1 {
  text-align: center;
  color: white;
  margin-bottom: 20px;
}

p {
  text-align: center;
  color: white;
  margin-bottom: 30px;
}
}
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  margin: 0;
  background-color: #121212; 
}
</style>
