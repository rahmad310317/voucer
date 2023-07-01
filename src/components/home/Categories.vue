<script setup>
import CategoriesCardVue from "../CategoriesCard.vue";

</script>
<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <!-- top categories -->
      <CategoriesCardVue />
    </div>
  </div>
</template>