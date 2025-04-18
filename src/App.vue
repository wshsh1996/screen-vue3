<template>
  <dv-full-screen-container class="container">
    <router-view></router-view>
  </dv-full-screen-container>
<!--  <full-screen-container class="container">-->
<!--    -->
<!--  </full-screen-container>-->
</template>

<script setup lang="ts">
import FullScreenContainer from "/@/components/FullScreenContainer/index.vue";
</script>

<style scoped>

.container {
  background: url("/src/assets/big_bg01.png");
  background-size: cover;
}
</style>
