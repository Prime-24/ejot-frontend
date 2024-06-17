<script lang="ts" setup>
defineProps<{
  backgroundImg: boolean;
  backgroundColor: 'white' | 'gray' | 'black' | 'red';
}>();
</script>

<template>
  <div :class="[`ej-teaser-wide--${backgroundColor}`, 'ej-teaser-wide']">
    <img v-if="backgroundImg" src="/img/rhino3.jpg" />
    <div
      :class="[
        backgroundImg ? 'absolute' : 'static mx-8 my-16',
        'ej-teaser-wide__content',
      ]"
    >
      <div class="ej-teaser-wide__img">
        <img src="/img/rhino3.jpg" />
      </div>
      <div class="ej-teaser-wide__text">
        <h2>Headline</h2>
        <p>
          A handcrafted, small-batch, artisinal pour-over version of the classic
          lorem ipsum generator, Hipster Ipsum will give your mocks that blue
          collar touch. Lorem ipsum dolor amet mustache knausgaard +1, blue
          bottle waistcoat tbh semiotics artisan synth stumptown gastropub
          cornhole celiac swag. Brunch raclette vexillologist post-ironic
          glossier ennui XOXO mlkshk godard pour-over blog tumblr humblebrag.
          Blue bottle put a bird on it twee prism biodiesel brooklyn. Blue
          bottle ennui tbh succulents.
        </p>
        <BaseLinkButton link-type="primary" :link-icon="true">
          Hier klicken</BaseLinkButton
        >
      </div>
    </div>
  </div>
</template>

<style>
.ej-teaser-wide {
  @apply relative flex;
}
.ej-teaser-wide--white {
  @apply bg-white;
}
.ej-teaser-wide--white .ej-teaser-wide__text {
  @apply text-black;
}
.ej-teaser-wide--black {
  @apply bg-black;
}
.ej-teaser-wide--black .ej-teaser-wide__text {
  @apply text-white;
}

.ej-teaser-wide--gray {
  @apply bg-gray-300 text-black;
}
.ej-teaser-wide--gray .ej-teaser-wide__text {
  @apply text-black;
}

.ej-teaser-wide--red {
  @apply bg-red-500;
}
.ej-teaser-wide--red .ej-teaser-wide__text {
  @apply text-white;
}

.ej-teaser-wide > img {
  @apply w-full brightness-[.33];
}

.ej-teaser-wide__content {
  @apply inset-y-16 inset-x-8 flex gap-8;
}

.ej-teaser-wide__img {
  @apply flex-1 flex items-center;
}
.ej-teaser-wide__img img {
  @apply w-full object-cover aspect-video;
}

.ej-teaser-wide__text {
  @apply flex-1 flex flex-col items-start gap-8 justify-center text-white;
}
.ej-teaser-wide__text h2 {
  @apply text-3xl font-bold;
}
</style>
