<template>
  <h1 class="text-6xl">This is About page.</h1>
</template>

<script setup lang="ts">
import { useStore } from '@/stores/main';
import { onMounted } from 'vue';

onMounted(() => {
  const mainStore = useStore()
  mainStore.count = mainStore.count + 1
})
</script>