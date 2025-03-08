<template>
  <div>user/index</div>
  <div>{{ route }}</div>
</template>
<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
</script>
<route lang="yaml">
meta:
  layout: admin
</route>
