<script setup>
import CategoryCard from "../CategoryCard.vue";
import { ref } from "vue";

const categories = ref([
  { id: 1, title: "Mobile UI Kit", count: 731, Image: "categories-1.jpg" },
  { id: 2, title: "font", count: 657, Image: "categories-2.jpg" },
  { id: 3, title: "icon Set", count: 83559, Image: "categories-3.jpg" },
  { id: 4, title: "Website Ui Kit", count: 4500, Image: "categories-4.jpg" },
]);
</script>
<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <!-- top categories -->

      <CategoryCard
        v-for="category in categories"
        :key="category.id"
        :id="category.id"
        :title="category.title"
        :count="category.count"
        :image="category.Image" />
    </div>
  </div>
</template>
