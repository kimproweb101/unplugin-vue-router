<template>
  <div>
    {{ route.meta }}
  </div>
</template>

<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
</script>

<style lang="scss" scoped></style>
<route lang="yaml">
name: home-page
meta:
  layout: ClientLayout
  requiresAuth: true
  width: 500px
</route>
