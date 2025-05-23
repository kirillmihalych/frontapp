<template>
  <div>
    <p class="mb-2 text-neutral-50 text-xl">Статус рассмотрения</p>
    <UStepper :items="resumeStatusList" class="w-full" orientation="vertical" />
  </div>
</template>

<script setup lang="ts">
const resumeStatusList = ref([
  {
    title: 'Новое',
  },
  {
    title: 'Просмотрено',
  },
  {
    title: 'Отправлено приглашение',
  },
  {
    title: 'Назначено собеседование',
  },
  {
    title: 'Не дошёл',
  },
  {
    title: 'Проведено собеседование',
  },
  {
    title: 'Ожидает ответа соискателя',
  },
  {
    title: 'Принятие решения',
  },
  {
    title: 'Принят',
  },
  {
    title: 'Отклонено',
  },
  {
    title: 'Архивировано',
  },
]);
</script>
