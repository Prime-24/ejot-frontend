<script setup lang="ts">
import Wrapper from './Wrapper.vue';

defineProps<{
  type: 'content' | 'full' | 'full-content';
  backgroundColor: 'red' | 'green' | 'blue';
}>();
</script>
<template>
  <Wrapper :type="type" :background-color="backgroundColor">
    <h1>Component One</h1>
  </Wrapper>
</template>
