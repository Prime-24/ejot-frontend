<script lang="ts" setup>
defineProps<{
  linkType: 'primary' | 'secondary' | 'normal-red' | 'normal-black';
}>();
</script>
<template>
  <NuxtLink :class="`ej-link-icon--${linkType}`" class="ej-link-icon">
    <Icon name="mdi:arrow-right" />
  </NuxtLink>
</template>

<style>
.ej-link-icon {
  @apply flex items-center py-4 px-8 cursor-pointer;
}
.ej-link-icon--normal-red {
  @apply text-red-500 hover:bg-red-500 hover:text-white;
}
.ej-link-icon--normal-black {
  @apply text-red-500 hover:bg-black hover:text-white;
}
.ej-link-icon--primary {
  @apply bg-red-500 text-white hover:bg-black hover:text-white;
}
.ej-link-icon--secondary {
  @apply bg-black text-white hover:bg-red-500 hover:text-white;
}
</style>
