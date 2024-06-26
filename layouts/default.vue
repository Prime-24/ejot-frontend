<template>
  <div class="flex flex-col gap-8">
    <nav class="bg-black text-white p-4">
      <ul class="flex flex-col md:flex-row gap-4">
        <li><NuxtLink to="/">Home</NuxtLink></li>
        <li><NuxtLink to="/Links">Link Components</NuxtLink></li>
        <li><NuxtLink to="/Teasers">Teaser Components</NuxtLink></li>
        <li><NuxtLink to="/Layout">Layout Components</NuxtLink></li>
        <li><NuxtLink to="/Contacts">Contacts Components</NuxtLink></li>
        <li><NuxtLink to="/Jumbos">Jumbo Components</NuxtLink></li>
      </ul>
    </nav>

    <div class="">
      <slot />
    </div>
  </div>
</template>
