<template>
  <div>
    <ChildComponent
        :message="parentMessage"
        @custom-event="handleEvent"/>
  </div>
</template>

<script setup lang='ts'>
import { ref, defineOptions } from 'vue'
import ChildComponent from './ChildComponent.vue'

defineOptions({ name: 'ParentComponent' })

const parentMessage = ref('Hello from parent')

const handleEvent = (data: string) =>
{
  console.log(data)
}
</script>
