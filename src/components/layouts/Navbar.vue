<script setup>
import { onMounted, computed } from "vue";
import { useUserStore } from "@/stores/user";

import Logo from "./Logo.vue";
import NavigationLinks from "./NavigationLinks.vue";
import UserInfo from "./UserInfo.vue";
import AutButton from "./AutButton.vue";

const userStore = useUserStore();
const isLoggedIn = computed(() => userStore.isLoggedIn);
const user = computed(() => userStore.user);

onMounted(() => {
  userStore.fetchuser;
});
</script>
<template>
  <Logo />
  <UserInfo v-if="isLoggedIn" :user="user.data" />
  <AutButton v-else />
  <NavigationLinks />
</template>
