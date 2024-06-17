<template>
  <NuxtLink class="ej-link-download">
    <Icon name="mdi:download" />
    <slot></slot>
  </NuxtLink>
</template>

<style>
.ej-link-download {
  @apply flex gap-4 items-center py-4 px-12 bg-black border border-black text-white hover:bg-white hover:text-black cursor-pointer;
}
</style>
