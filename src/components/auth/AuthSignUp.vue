<template>
  <div class="modal-header">
    <div class="modal-title text-center">회원가입</div>
  </div>
  <div class="modal-contents">contents</div>
  <div class="modal-footer d-flex space-between">
    <button type="button" @click="$emit('change-view', 'SignIn')">로그인</button>
  </div>
</template>

<script setup>
defineEmits(['change-view'])
</script>

<style lang="scss" scoped></style>
