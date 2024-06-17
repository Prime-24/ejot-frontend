<script lang="ts" setup>
defineProps<{
  isDivided: boolean;
}>();
</script>

<template>
  <ul :class="[{ 'ej-list-links--divider': isDivided }, 'ej-list-links']">
    <BaseListLink :linkType="isDivided ? 'normal' : 'primary'"
      >Geschäftsführung</BaseListLink
    >
    <BaseListLink :linkType="isDivided ? 'normal' : 'primary'"
      >Vision, Marke</BaseListLink
    >
    <BaseListLink :linkType="isDivided ? 'normal' : 'primary'"
      >Historie</BaseListLink
    >
    <BaseListLink :linkType="isDivided ? 'normal' : 'primary'"
      >Compliance</BaseListLink
    >
  </ul>
</template>

<style>
.ej-list-links {
  @apply flex flex-col gap-2;
}
.ej-list-links--divider {
  @apply divide-y divide-black;
}
</style>
