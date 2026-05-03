<script setup lang="ts">
import { onMounted } from 'vue'
import { navigateTo } from '#app'

// Use client-side auth token to decide where to redirect
const { getToken } = useAuthToken()

onMounted(() => {
  const token = getToken()
  if (token) {
    navigateTo('/dashboard/links')
  }
  else {
    navigateTo('/dashboard/login')
  }
})
</script>

<template>
  <div />
</template>
