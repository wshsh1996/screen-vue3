<template>
  <div id="dv-full-screen-container" ref="fullScreenContainer">
    <template v-if="state.ready">
      <slot />
    </template>
  </div>
</template>

<script lang="ts" setup>
import { reactive, ref } from 'vue';
import autoResize from '/@/utils/autoResize';

const fullScreenContainer = ref<HTMLElement | null>(null);

const state = reactive({
  allWidth: 0,
  scale: 0,
  datavRoot: '',
  ready: false,
});

// 修改: 动态获取屏幕宽高
const initConfig = () => {
  const screenWidth = window.innerWidth;
  const screenHeight = window.innerHeight;

  // 根据屏幕宽高设置容器的宽高比例
  let width = screenWidth;
  let height = screenHeight;

  state.allWidth = width;

  if (fullScreenContainer.value) {
    fullScreenContainer.value.style.width = `${width}px`;
    fullScreenContainer.value.style.height = `${height}px`;
  }
};

// 修改: 根据当前屏幕宽度动态设置缩放比例
const setAppScale = () => {
  const currentWidth = document.body.clientWidth;
  if (fullScreenContainer.value) {
    fullScreenContainer.value.style.transform = `scale(${currentWidth / state.allWidth})`;
  }
};

const onResize = () => {
  setAppScale();
};

const afterAutoResizeMixinInit = () => {
  initConfig();
  setAppScale();

  state.ready = true;
};

autoResize(fullScreenContainer, onResize, afterAutoResizeMixinInit);
</script>

<style lang="scss">
#dv-full-screen-container {
  position: fixed;
  top: 0px;
  left: 0px;
  overflow: hidden;
  transform-origin: left top;
  z-index: 999;
    /*width: 100vw !important;
    height: 100vh !important;*/
}
</style>
