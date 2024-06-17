<template>
  <div class="flex flex-col gap-8 m-8">
    <nav>
      <ul class="flex gap-4">
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/Links">Link Components</NuxtLink></li>
        <li><NuxtLink to="/Teasers">Teaser Components</NuxtLink></li>
        <li><NuxtLink to="/Layout">Layout Components</NuxtLink></li>
        <li><NuxtLink to="/Contact">Contact Components</NuxtLink></li>
      </ul>
    </nav>

    <slot />
  </div>
</template>
