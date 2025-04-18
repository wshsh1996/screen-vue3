<template>
  <div class="home-container">
    <!-- 标题 -->
    <TopHeader @toggle-form="changeActive"></TopHeader>

    <div v-if="active === 1" class="flex p-10" >
      <!-- 第一个 -->
      <div class="flex1 " >
        <First></First>
      </div>

      <!-- 第二个 -->
      <div class="flex1" >
        <Second></Second>
      </div>
    </div>
    <div v-if="active === 2" class="flex p-10" >
      <!-- 第三个 -->
            <div class="flex1 " >
              <Third></Third>
            </div>

      <!-- 第四个 -->
            <div class="flex1 " >
              <Forth></Forth>
            </div>
    </div>
    <div v-if="active === 3" class="flex p-10" >
      <!-- 第五个 -->
            <div class="flex1 ">
              <Fifth></Fifth>
            </div>

      <!-- 第六个 -->
            <div class="flex1 ">
              <Sixth></Sixth>
            </div>
    </div>
  </div>
</template>

<script lang="ts" setup>


// 第一個
import First from "/@/components/FirstComponent/index.vue";
import Second from "/@/components/SecondComponent/index.vue";
import Third from "/@/components/ThirdComponent/index.vue";

import Forth from "/@/components/ForthComponent/index.vue";
import Fifth from "/@/components/FifthComponent/index.vue";
import Sixth from "/@/components/SixthComponent/index.vue";

import TopHeader from "/@/components/TopHeader/index.vue";
import {ref} from "vue";

const active = ref(1)

const changeActive = () => {
  if(active.value === 3) {
    active.value = 1
  } else {
    active.value++
  }
  console.log(active.value,'aaaa')
}

</script>
<style lang="scss" scoped>

</style>

