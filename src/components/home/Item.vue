<script setup>
import NewItemCard from "../NewItemCard.vue";
import { ref } from "vue";

const NewItem = ref([
  {
    id: 1,
    title: "Mobile UI Kit",
    subTitle: "Mobile UI Kit",
    Image: "items-1.jpg",
  },
  {
    id: 2,
    title: "Online Doctor Consultation",
    subTitle: "Mobile UI Kit",
    Image: "items-2.jpg",
  },
  {
    id: 3,
    title: "Banking Crypto",
    subTitle: "Mobile UI Kit",
    Image: "items-3.jpg",
  },
]);
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
