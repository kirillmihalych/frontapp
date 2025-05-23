<template>
  <div>
    <p class="mb-2 text-neutral-50 text-xl">Дела</p>
    <div class="flex gap-2">
      <UButton
        v-for="(btn, index) in toDoBtns"
        :key="index"
        class="w-[150px] bg-neutral-50"
        :class="[btn.active ? 'bg-primary' : 'bg-neutral-50']"
      >
        {{ btn.name }}
      </UButton>
    </div>
  </div>
</template>

<script setup lang="ts">
const toDoBtns = ref([
  {
    active: true,
    name: 'Собеседование запланировано',
  },
  {
    active: false,
    name: 'Создать видеозвонок',
  },
  {
    active: false,
    name: 'Запланировать собеседование',
  },
  {
    active: false,
    name: 'Отправить запрос',
  },
]);
</script>
