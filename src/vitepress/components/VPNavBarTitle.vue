<script setup lang="ts">
import { useData, withBase } from 'vitepress'

const { site } = useData()
</script>

<template>
  <a class="VPNavBarTitle" href="/">
    <img class="logo" :src="withBase('/icons/apple-touch-icon.png')" />
    <span class="text">{{ site.title }}</span>
  </a>
</template>

<style scoped>
.VPNavBarTitle {
  display: flex;
  align-items: center;
  padding-top: 1px;
  height: var(--vt-nav-height);
  transition: opacity 0.25s;
}

.VPNavBarTitle:hover {
  opacity: 0.6;
}

.logo {
  position: relative;
  width: 36px;
  height: 36px;
  border-radius: 5px;
}

.logo + .text {
  padding-left: 10px;
}

.text {
  font-size: 18px;
  font-weight: 500;
}
</style>
