<template>
  <div class="flex gap-2 mb-4">
    <UButton
      v-for="(btn, index) in btns"
      :key="index"
      class="size-8 lg:size-12 flex items-center justify-center"
    >
      <Icon :name="btn.icon" />
    </UButton>
  </div>
</template>

<script setup lang="ts">
const btns = ref([
  { icon: 'lucide:printer' },
  {
    icon: 'ic:baseline-picture-as-pdf',
  },
  {
    icon: 'lucide:user-round-pen',
  },
  {
    icon: 'lucide:trash-2',
  },
  {
    icon: 'lucide:file-input',
  },
  {
    icon: 'lucide:heart',
  },
]);
</script>
