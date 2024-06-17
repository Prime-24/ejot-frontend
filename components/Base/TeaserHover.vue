<script lang="ts" setup>
const props = defineProps<{
  type: 'black' | 'white';
}>();
</script>

<template>
  <div :class="[`ej-teaser-hover--${type}`, 'ej-teaser-hover']">
    <img src="/img/rhino2.jpg" class="" />
    <div class="ej-teaser-hover__headline">
      <h2>Hello World</h2>
      <div class="relative p-4">
        <Icon
          class="ej-teaser-hover__icon--plus ej-teaser-hover__icon"
          name="mdi:plus"
        />
        <Icon
          class="ej-teaser-hover__icon-minus ej-teaser-hover__icon"
          name="mdi:minus"
        />
      </div>
    </div>
    <div class="ej-teaser-hover__content">
      <h2>here goes the content malaka</h2>
      <p>klasdjflkö aklsdjfölk adijfo ieiohadf ölidafio ekahnsdkf oiadhjfoie</p>
    </div>
  </div>
</template>

<style>
.ej-teaser-hover {
  @apply relative overflow-hidden isolate w-96;
}
.ej-teaser-hover--black {
  @apply bg-black/50 text-white;
}
.ej-teaser-hover--white {
  @apply bg-white/50;
}

.ej-teaser-hover__headline {
  @apply bg-inherit flex items-center justify-between p-4 absolute bottom-0 inset-x-0 transition-all duration-300 z-[2];
}

.ej-teaser-hover__content {
  @apply absolute flex flex-col gap-4 p-4 bg-inherit h-full w-full transition-all duration-300;
}

.ej-teaser-hover__icon {
  @apply absolute left-1/2 top-1/2 -translate-y-1/2;
}

.ej-teaser-hover:hover .ej-teaser-hover__content {
  @apply -translate-y-full;
}
.ej-teaser-hover:hover .ej-teaser-hover__headline {
  @apply bg-transparent;
}
.ej-teaser-hover:hover .ej-teaser-hover__headline h2 {
  @apply invisible;
}
.ej-teaser-hover:hover .ej-teaser-hover__icon--plus {
  @apply hidden;
}
</style>
