<template>
  <div>
    <p>{{ message }}</p>
    <button @click="$emit('custom-event',
    'Hello from child')">Send Event</button>
  </div>
</template>

<script setup lang='ts'>
import { defineProps, defineEmits, defineOptions } from 'vue'

defineOptions({ name: 'ChildComponent' })

const props = defineProps({
  message: {
    type: String,
    required: true
  }
})

const emit = defineEmits(['custom-event'])
</script>
