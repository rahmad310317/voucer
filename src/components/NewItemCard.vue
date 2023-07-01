<script setup>
import { RouterLink } from 'vue-router';

</script>
<template>
  <div class="w-full px-1 my-1 md:w-1/2 lg:my-4 lg:px-4 lg:w-1/3">
    <div class="overflow-hidden border border-gray-200 rounded-xl">
      <RouterLink to="/details">
        <div class="m-4 overflow-hidden rounded-xl">
          <img alt="Placeholder" class="block w-full h-auto" src="@/assets/img/items-1.jpg" />
        </div>
      </RouterLink>

      <header class="px-4 mb-4 leading-tight">
        <h1 class="text-lg">
          <a class="font-semibold text-black no-underline hover:underline" href="#">
            Mobile UI Kit
          </a>
        </h1>
        <span class="block text-sm font-light text-gray-500 no-underline">
          Mobile UI Kit
        </span>
      </header>
    </div>
  </div>
</template>