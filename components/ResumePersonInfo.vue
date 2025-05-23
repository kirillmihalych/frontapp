<template>
  <div v-if="data" class="flex flex-col lg:flex-row gap-4 mb-4">
    <img :src="baseURL + data.photo" class="size-[200px]" />
    <div class="text-lg">
      <ULink to="#" class="text-2xl font-bold text-neutral-50"
        >{{ data.name }}<Icon name="lucide:external-link"
      /></ULink>
      <div class="flex flex-col md:flex-row gap-1">
        <p>Кандидат на вакансию:</p>
        <ULink to="#" class="text-primary"
          >Жадный благотворитель <span>(14.08.2024 Отклик)</span>
          <Icon name="lucide:external-link"
        /></ULink>
      </div>
      <p>Просмотрено</p>
      <p>Возраст не указан</p>
      <div class="flex items-center gap-2">
        <Icon name="ic:baseline-local-phone" />
        <ULink to="#" class="text-primary">+79876543210</ULink>
        <Icon name="ic:baseline-telegram" />
        <Icon name="ic:outline-whatsapp" />
      </div>
      <div class="flex items-center gap-2">
        <Icon name="ic:baseline-mail" />
        <ULink to="#" class="text-primary">test@gmail.com</ULink>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const baseURL = 'https://dev.jobcart.ru/';

const { data } = useAsyncData('resume', () =>
  $fetch('https://dev.jobcart.ru/wp-json/test/v2/app')
);
</script>
