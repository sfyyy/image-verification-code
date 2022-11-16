<script setup lang="ts">
import background from "@/assets/image/1.jpeg";
import Icon from "@/components/icon/love.vue";
</script>

<template>
  <div class="verification-code">
    <div
      class="content"
      :style="{
        background: `url(${background}) no-repeat 100% 100%`,
        backgroundSize: '100% 100%',
      }"
    >
      <Icon
        :style="{
          width: '48px',
          height: '48px',
          color: '#d00',
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
</style>
