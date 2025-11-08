<template>
  <div>
    <input v-model="id" />
    <input v-model="password" />
    <p>{{ message }}</p>
    <button @click="whoami">whoami</button>
  </div>
</template>

<script setup lang="ts">
import { ref, defineOptions } from 'vue'

defineOptions({ name: 'E03Binding' })

const id = ref('ID ')
const password = ref('PASSWORD')
const message = ref('로그인하세요')

const whoami = () =>
{
  message.value = id.value + ' ' + password.value
}
</script>
