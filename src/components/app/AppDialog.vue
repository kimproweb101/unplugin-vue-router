<template>
  <div class="modal-header d-flex space-between">
    <div class="modal-title">로그인</div>
    <button type="button" class="modal-btn-close" @click="$emit('modal-close')">X</button>
  </div>
  <div class="modal-contents">contents</div>
  <div class="modal-footer d-flex space-between">
    <button type="button" @click="$emit('AuthFindPassword')">비밀번호 찾기</button>
    <button type="button" @click="$emit('AuthSignUp')">이메일 가입하기</button>
  </div>
</template>
