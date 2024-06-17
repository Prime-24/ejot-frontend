<template>
  <div class="flex flex-col gap-8 items-start">
    <h1 class="text-3xl">Link Components</h1>
    <BaseLinkButton link-type="primary" :link-icon="true"
      >Mehr Erfahren</BaseLinkButton
    >

    <BaseLinkDownload>Broschüre downloaden</BaseLinkDownload>

    <BaseLinkIcon linkType="normal-black" />
    <BaseListLink linkType="primary">Geschäftsführung</BaseListLink>
    <BaseListLinks :is-divided="false" />
    <BaseLink>Zur Broschüre</BaseLink>
  </div>
</template>
