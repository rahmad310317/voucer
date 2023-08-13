<script setup>
import { onMounted, computed } from "vue";
import { useUserStore } from "@/stores/user";

import Logo from "./Logo.vue";
import NavigationLinks from "./NavigationLinks.vue";
import UserInfo from "./UserInfo.vue";

const userStore = useUserStore();
const isLoggedIn = computed(() => userStore.isLoggedIn);
const getUser = computed(() => userStore.getUser);
const user = computed(() => userStore.user);

onMounted(() => {
  userStore.fetchuser;
});
</script>
<template>
  <Logo />
  <NavigationLinks />
  <UserInfo />
</template>
