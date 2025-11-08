<template>
  <div>Hello, {{ message }}</div>
</template>

<script setup lang='ts'>
import { ref, defineOptions } from 'vue'

defineOptions({name: 'E01Instance'})

const name = 'Seokmin'
const message = ref<string>(name)
</script>

<style scoped>
div
{
  color: blue;
  font-size: 20px;
  font-weight: bold;
}
</style>
