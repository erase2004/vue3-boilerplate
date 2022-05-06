<template>
  <div class="self-center">
    <router-link
      :to="{name: 'home'}"
      class="font-bold"
    >
      Home
    </router-link> |
    <router-link
      :to="{name: 'about'}"
      class="font-bold"
    >
      About
    </router-link>
  </div>
  <div class="self-center my-4">
    <router-view></router-view>
  </div>
  <div class="self-center">
    Count: {{ mainStore.count }}
  </div>
</template>

<script setup lang="ts">
import { useStore } from '@/stores/main';
const mainStore = useStore()
</script>

<style lang="postcss">
.router-link-exact-active {
  @apply text-green-700;
}
</style>