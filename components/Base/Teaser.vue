<script lang="ts" setup>
defineProps<{
  background: 'white' | 'gray' | 'black' | 'red';
  isButton: boolean;
  hasLink: boolean;
  linkBtnType: 'primary' | 'secondary' | 'normal-red' | 'normal-black';
  badgeText: string;
}>();
</script>

<template>
  <div class="ej-teaser">
    <img src="/img/rhino.jpg" class="ej-teaser__img" />
    <div :class="[`ej-teaser__text--${background}`, 'ej-teaser__text']">
      <span v-if="badgeText" class="ej-teaser__badge">{{ badgeText }}</span>
      <h2 class="ej-teaser__text-headline">Lorem ipsum</h2>
      <p>
        jklöadjf löaksdj flköasdj fasdlköjf lköasdjdf aösdlkf jlasködjf
        klöasdhfuihuiheiul ajklödhffkjahfeuih ö klöadsjhfasdöjkj hjka
        hioöasdhfadlifu
      </p>
      <template v-if="hasLink">
        <div v-if="isButton && background === 'white'" class="ej-teaser__btn">
          <BaseLinkButton :link-type="linkBtnType" :link-icon="true"
            >Mehr Erfahren</BaseLinkButton
          >
        </div>
        <div v-else class="ej-teaser__link">
          <Icon name="mdi:arrow-right" />
        </div>
      </template>
    </div>
  </div>
</template>

<style>
.ej-teaser {
  @apply grid gap-0 col-span-1 row-span-2 grid-rows-subgrid;
}
.ej-teaser__img {
  @apply w-full h-full object-cover;
}
.ej-teaser__text {
  @apply relative flex flex-col gap-4 p-4 border border-transparent before:absolute before:top-0 before:left-[-1px] before:right-[-1px] before:h-3 before:bg-inherit;
}
.ej-teaser__text--white {
  @apply bg-white border-black;
}
.ej-teaser__text--gray {
  @apply bg-gray-300 text-black;
}
.ej-teaser__text--black {
  @apply bg-black text-white;
}
.ej-teaser__text--red {
  @apply bg-red-500 text-white border-red-500;
}
.ej-teaser__text-headline {
  @apply text-2xl font-bold uppercase md:text-3xl;
}

.ej-teaser__badge {
  @apply relative self-start p-4 -mt-12 text-white font-bold uppercase;
}

.ej-teaser__badge--red {
  @apply bg-red-500;
}

.ej-teaser__badge--black {
  @apply bg-red-500;
}

.ej-teaser__btn {
  @apply relative bg-white pt-4 pl-4 self-end mb-[-17px] mr-[-17px];
}
.ej-teaser__link {
  @apply relative pt-4 pl-4 self-end text-red-500;
}

.ej-teaser__text--black .ej-teaser__link,
.ej-teaser__text--red .ej-teaser__link {
  @apply text-white;
}
.ej-teaser__text--black .ej-teaser__badge,
.ej-teaser__text--gray .ej-teaser__badge,
.ej-teaser__text--white .ej-teaser__badge {
  @apply bg-red-500;
}
.ej-teaser__text--red .ej-teaser__badge {
  @apply bg-black;
}
</style>
