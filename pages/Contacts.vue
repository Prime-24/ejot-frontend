<script setup lang="ts">
defineProps<{
  border: boolean;
}>();
</script>
<template>
    <h2 class="text-2xl">Contacts Card</h2>
    <div class="flex flex-wrap gap-8">
        <BaseContact :border="true"/>
        <BaseContact :border="false"/>
    </div>
</template>