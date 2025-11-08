<template>
  <div>{{ fullName }}</div>
</template>

<script setup lang='ts'>
import { ref, computed, onMounted, defineOptions } from 'vue'

defineOptions({ name: 'E02Reactive' })

const firstName = ref('Seokmin')
const lastName = ref('Kang')

const fullName = computed(() => `${firstName.value} ${lastName.value}`)

onMounted(() =>
{
  console.log('mounted')

  setTimeout(() =>
  {
    lastName.value = 'Gang'
  }, 2000)
})
</script>
