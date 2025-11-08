<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script setup lang='ts'>
import { provide, defineOptions } from 'vue'
import ChildComponent1 from '@/components/example4/ChildComponent1.vue'

defineOptions({ name: 'E06ParentComponent' })

provide('sharedMessage', 'Hello from provide')
</script>
