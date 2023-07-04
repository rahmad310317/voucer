<script setup>
import Login from "../components/authentication/login.vue";
</script>

<template>
  <div class="relative overflow-hidden bg-white">
    <div class="mx-auto max-w-7xl">
      <div
        class="flex flex-col items-center w-full min-h-screen pt-6 sm:justify-center sm:pt-0">
        <!-- login Form -->
        <Login />
        <div class="w-full mx-auto mt-20 sm:max-w-2xl">
          <img src="img/brand-logo.svg" alt="" class="w-full px-10 md:px-0" />
        </div>
      </div>
    </div>
  </div>
</template>
