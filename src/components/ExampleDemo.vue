<template>
  <div>
    子组件
    <ExampleSonDemoVue :visible="visible" @close="changeVisible" />
  </div>
</template>

<script setup lang="ts">
import ExampleSonDemoVue from "./ExampleSonDemo.vue";
import { ref } from 'vue'
const visible = ref(true)

const changeVisible = (val) => {
  visible.value = val
}
</script>

<style lang='scss' scoped>
</style>