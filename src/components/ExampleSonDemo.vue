<template>
  <div>我是父 {{ visible }}

    <button @click="closeFn">关闭</button>
  </div>
</template>

<script setup lang="ts">
defineProps({
  visible: {
    type: Boolean,
    default: false
  }
})

const emits = defineEmits(['close'])

const closeFn = () => {
  emits('close', false)
}
</script>
<style lang='scss' scoped>
</style>