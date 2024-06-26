<template>
  <div class="teasers">
    <div class="teasers__upper-background"></div>
    <h2 class="teasers__headline p-4">Hier könnte ihre Überschrift stehen</h2>
    <div class="teasers__wrapper">
      <BaseTeaser background="white" :has-link="true" :is-button="true" link-btn-type="primary" badge-text="New" />
      <BaseTeaser background="white" :has-link="true" :is-button="true" link-btn-type="primary" badge-text="New" />
      <BaseTeaser background="white" :has-link="true" :is-button="true" link-btn-type="primary" badge-text="New" />
      <BaseTeaser background="white" :has-link="true" :is-button="true" link-btn-type="primary" badge-text="New" />
    </div>
  </div>
</template>

<style>
.teasers {
  display: grid;
  grid-template-columns: 1fr min(100%, 1600px) 1fr;
  grid-template-rows: repeat(9, auto);
}

.teasers__headline {
  display: flex;
  align-items: center;
  color: orange;
  font-size: 2rem;
  grid-row: 1;
  grid-column: 2;
}

.teasers__upper-background {
  background-color: black;
  grid-column: 1 / -1;
  grid-row: 1 / 3;
}

.teasers__wrapper {
  grid-column: 2/ -2;
  grid-row: 2/ -1;
  display: grid;
  gap: 1rem;
  padding: 1rem;
  grid-template-columns: repeat(auto-fit, minmax(min(300px, 100%), 1fr));
  grid-template-rows: subgrid;
  grid-auto-rows: auto;
}
</style>
