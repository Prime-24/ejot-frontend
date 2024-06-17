<script setup lang="ts">
let component1 = resolveComponent('CompoOne');
let component2 = resolveComponent('CompoTwo');

let components = { component1, component2 };
</script>

<template>
  <div class="layout">
    <CompoOne type="full" background-color="red"></CompoOne>
    <CompoOne type="content" background-color="green"></CompoOne>
    <CompoOne type="full-content" background-color="blue"></CompoOne>

    <component
      v-bind="{ type: 'full-content', backgroundColor: 'red' }"
      :is="components['component2']"
    ></component>
  </div>
</template>
