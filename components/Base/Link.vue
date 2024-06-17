<template>
  <NuxtLink class="ej-link">
    <slot></slot>
  </NuxtLink>
</template>

<style>
.ej-link {
  @apply flex items-center underline font-bold hover:text-red-500;
}
</style>
