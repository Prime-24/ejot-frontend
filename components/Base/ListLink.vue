<script lang="ts" setup>
defineProps<{
  linkType: 'primary' | 'normal';
}>();
</script>

<template>
  <NuxtLink :class="[`ej-list-link--${linkType}`, 'ej-list-link']">
    <Icon name="mdi:arrow-right" color="red" />
    <slot></slot>
  </NuxtLink>
</template>

<style>
.ej-list-link {
  @apply flex items-center gap-4 p-4 cursor-pointer;
}

.ej-list-link--normal {
  @apply hover:text-red-500;
}
.ej-list-link--primary {
  @apply bg-gray-300 border border-gray-300 hover:border-red-500;
}
</style>
