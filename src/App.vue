<template>
  <el-config-provider namespace="ep" :locale="locale">
    <BaseHeader />
    <div class="flex main-container">
      <BaseSide />
      <div w="full" py="4">
        <Logos my="4" />
        <HelloWorld msg="Vue 3 + Element Plus + Vite" />
      </div>
    </div>
  </el-config-provider>
</template>

<script>
import { defineComponent } from 'vue'
import zhCn from 'element-plus/dist/locale/zh-cn.mjs'
export default defineComponent({
  setup() {
    return {
      locale: zhCn,
    }
  },
})
</script>

<style>
#app {
  text-align: center;
  color: var(--ep-text-color-primary);
}

.main-container {
  height: calc(100vh - var(--ep-menu-item-height) - 4px);
}
</style>
