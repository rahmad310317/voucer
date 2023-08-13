<script setup>
import NewItemCard from "../NewItemCard.vue";
import { onMounted, ref } from "vue";
import axios from "axios";

const NewItem = ref([]);

async function getItemData() {
  try {
    const respone = await axios.post(
      "https://zullkit-backend.belajarkoding.com/api/products"
    );
    const NewItem = respone.value.data.data;
  } catch (error) {
    console.log(error);
  }
}

onMounted(() => {
  getItemData();
})
</script>

<template>
  <div class="container px-4 mx-auto my-16 md:px-12">
    <h2 class="mb-4 text-xl font-medium md:mb-0 md:text-lg">New Items</h2>
    <div class="flex flex-wrap -mx-1 lg:-mx-4">
      <!-- NewItem Card -->
      <NewItemCard
        v-for="item in NewItem"
        :key="item.id"
        :id="item.id"
        :title="item.title"
        :subTitle="item.subTitle"
        :image="item.Image" />
    </div>
  </div>
</template>
