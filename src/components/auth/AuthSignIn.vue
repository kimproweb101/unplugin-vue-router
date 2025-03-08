<template>
  <div class="modal-header">
    <div class="modal-title text-center">로그인</div>
  </div>
  <div class="modal-contents">contents</div>
  <div class="modal-footer d-flex space-between">
    <button type="button" @click="$emit('change-view', 'FindPassword')">비밀번호 찾기</button>
    <button type="button" @click="$emit('change-view', 'SignUp')">이메일 가입하기</button>
  </div>
</template>

<script setup>
defineEmits(['change-view'])
</script>

<style lang="scss" scoped></style>
