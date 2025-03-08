<template>
  <div class="wrapper">
    <div class="header">
      header
    </div>
    <router-view />
    <AuthDialog v-model="dialog" @modalClose="dialog = false" />
  </div>
</template>
<script setup>
import AuthDialog from '@/components/auth/AuthDialog.vue';
import { ref } from 'vue';
const dialog = ref(true)
</script>
<style sciped></style>
