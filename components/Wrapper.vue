<script setup lang="ts">
defineProps<{
  type: 'content' | 'full' | 'full-content';
  backgroundColor: 'red' | 'green' | 'blue';
}>();
</script>

<template>
  <div
    :class="{
      content: type === 'content',
      full: type === 'full',
      'full full-content': type === 'full-content',
      'bg-red-500': backgroundColor === 'red',
      'bg-blue-500': backgroundColor === 'blue',
      'bg-green-500': backgroundColor === 'green',
    }"
  >
    <slot></slot>
  </div>
</template>
