<script setup lang="ts">
import background from "@/assets/image/1.jpeg";
import Icon from "@/components/icon/canMovePuzzleIcon.vue";
import BlockIcon from "@/components/icon/blockIcon.vue";
import { onMounted, ref } from "vue";
const canMoveCanvas = ref<HTMLCanvasElement>();
const canMoveIconRef = ref();
// canMoveCanvas.value.getContext("2d").drawImage(background, 0, 0, 200, 200);
onMounted(() => {
  // const ctx = canMoveCanvas.value?.getContext("2d");
  // if (ctx) {
  // }
});
</script>

<template>
  <div class="verification-code">
    <div
      class="content"
      :style="{
        background: `url(${background}) no-repeat 100% 100%`,
        backgroundSize: '100% 100%',
        position: 'relative',
      }"
    >
      <img :src="background" alt="" />

      <Icon
        ref="canMoveIconRef"
        :style="{
          width: '48px',
          height: '48px',
          cursor: 'pointer',
        }"
      />
      <BlockIcon
        :style="{
          width: '48px',
          height: '48px',
          position: 'absolute',
          top: '0',
          left: '100px',
          color: '#fff',
          opacity: '1',
        }"
      />
    </div>
  </div>
</template>

<style scoped>
.verification-code {
  width: 400px;
  height: 250px;
}

.content {
  width: 100%;
  height: 100%;
}

img {
  position: absolute; /* absolute或fixed定位是必须的 */
  clip-path: url(#svgPath);
}
</style>
