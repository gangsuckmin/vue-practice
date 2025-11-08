<template>
  <div>
    <p>{{ sharedMessage }}</p>
  </div>
</template>

<script setup lang='ts'>
import { inject, defineOptions } from 'vue'

defineOptions({ name: 'ChildComponent2' })

const sharedMessage = inject('sharedMessage')
</script>

<style scoped>
  p
  {
    font-size: 1.5rem;
  }
</style>
