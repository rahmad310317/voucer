<script setup>
import CategoryCard from "../CategoryCard.vue";
import axios from "axios";
import { onMounted, ref } from "vue";

const categories = ref([]);

// Call Api

async function getDataCategories() {
  try {
    const respone = await axios.get(
      "https://zullkit-backend.belajarkoding.com/api/categories?limit=4"
    );
    const categories = respone.value.data.data;
  } catch (error) {
    console.log(error);
  }
}

onMounted(() => {
  getDataCategories;
});
</script>
<template>
  <div class="container px-4 mx-auto my-16 md:px-12" id="categories">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">Top Categories</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <!-- top categories -->

      <CategoryCard
        v-for="category in categories"
        :key="category.id"
        :id="category.id"
        :title="category.name"
        :count="category.products_count"
        :image="category.thumbnails" />
    </div>
  </div>
</template>
