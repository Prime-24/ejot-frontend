<script setup lang="ts">
defineProps<{
  border: boolean;
}>();
</script>
<template>
    <div :class="[{'border border-black': border} ,'flex flex-wrap max-w-[500px]']">
        <div class="flex-grow basis-40">
            <img class="aspect-square w-full h-full object-cover" src="/img/rhino-avatar.png">
        </div>
        <div class="flex flex-col flex-grow-[3] gap-8 p-8 justify-center">
            <div>
                <h3 class="font-bold">Richard Nashorn</h3>
                <p class="font-semibold">Vertriebsingenieur</p>
            </div>
            <div>
                <p>M +Telefonnummer</p>
                <p>batman@gotham.de</p>
            </div>
        </div>
    </div>
</template>