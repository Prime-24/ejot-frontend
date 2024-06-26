<script lang="ts" setup>
defineProps<{
  linkType: 'primary' | 'secondary' | 'normal-red' | 'normal-black';
  linkIcon: boolean;
}>();
</script>

<template>
  <NuxtLink :class="[`ej-link-btn--${linkType}`, 'ej-link-btn']">
    <slot></slot>
    <Icon class="ej-link-btn__icon" v-if="linkIcon" name="mdi:arrow-right" />
  </NuxtLink>
</template>

<style>
.ej-link-btn {
  @apply inline-flex items-center gap-4 py-2 px-4 hover:text-white cursor-pointer;
}

.ej-link-btn--normal-red {
  @apply bg-white border border-black text-black hover:bg-red-500 hover:border-red-500;
}
.ej-link-btn--normal-red .ej-link-btn__icon {
  @apply text-red-500;
}
.ej-link-btn--normal-red:hover .ej-link-btn__icon {
  @apply text-white;
}

.ej-link-btn--normal-black {
  @apply bg-white border border-black text-black hover:bg-black hover:border-black;
}
.ej-link-btn--normal-black .ej-link-btn__icon {
  @apply text-red-500;
}
.ej-link-btn--normal-black:hover .ej-link-btn__icon {
  @apply text-white;
}

.ej-link-btn--primary {
  @apply bg-red-500 text-white hover:bg-black;
}

.ej-link-btn--secondary {
  @apply bg-black text-white hover:bg-red-500;
}
</style>
